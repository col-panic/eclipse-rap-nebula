### Trying to port [Nebula CDateTime](https://www.eclipse.org/nebula/widgets/cdatetime/cdatetime.php) to [Eclipse RAP](https://www.eclipse.org/rap/) as a standalone bundle.

The bundle org.eclipse.rap.nebula.widgets.cdatetime combines the following bundles to provide a standalone RAP CDateTime

* org.eclipse.nebula.cwt
* org.eclipse.rap.draw2d.compatibility
* org.eclipse.nebula.widgets.cdatetime

The following problems, considering the current RAP e4 (nightly i.e. 3.13) target exist:

* (org.eclipse.nebula.cwt.animation.ScrollingSmoother) org.eclipse.swt.widgets.Scrollbar#getIncrement() is not implemented - see https://bugs.eclipse.org/bugs/show_bug.cgi?id=360794
* (org.eclipse.nebula.cwt.v.VButtonPainter) new Image(Display, Rectangle) is not supported - see https://bugs.eclipse.org/bugs/show_bug.cgi?id=318900
* (org.eclipse.nebula.cwt.v.VButtonImageBak) gc.copyArea is not supported - see https://www.eclipse.org/rap/developers-guide/devguide.php?topic=rwt.html - Painting Limitations
