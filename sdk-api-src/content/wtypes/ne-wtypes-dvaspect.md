---
UID: NE:wtypes.tagDVASPECT
title: DVASPECT (wtypes.h)
description: Specifies the desired data or view aspect of the object when drawing or getting data.
helpviewer_keywords: ["DVASPECT","DVASPECT enumeration [COM]","DVASPECT_CONTENT","DVASPECT_DOCPRINT","DVASPECT_ICON","DVASPECT_THUMBNAIL","_ole_DVASPECT","com.dvaspect","wtypes/DVASPECT","wtypes/DVASPECT_CONTENT","wtypes/DVASPECT_DOCPRINT","wtypes/DVASPECT_ICON","wtypes/DVASPECT_THUMBNAIL"]
old-location: com\dvaspect.htm
tech.root: com
ms.assetid: a2b729c8-7091-4520-93cd-c44468ba0274
ms.date: 12/05/2018
ms.keywords: DVASPECT, DVASPECT enumeration [COM], DVASPECT_CONTENT, DVASPECT_DOCPRINT, DVASPECT_ICON, DVASPECT_THUMBNAIL, _ole_DVASPECT, com.dvaspect, wtypes/DVASPECT, wtypes/DVASPECT_CONTENT, wtypes/DVASPECT_DOCPRINT, wtypes/DVASPECT_ICON, wtypes/DVASPECT_THUMBNAIL
f1_keywords:
- wtypes/DVASPECT
dev_langs:
- c++
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WTypes.h
api_name:
- DVASPECT
targetos: Windows
req.typenames: DVASPECT
req.redist: 
ms.custom: 19H1
---

# DVASPECT enumeration


## -description


Specifies the desired data or view aspect of the object when drawing or getting data.




## -enum-fields




### -field DVASPECT_CONTENT

Provides a representation of an object so it can be displayed as an embedded object inside of a container. This value is typically specified for compound document objects. The presentation can be provided for the screen or printer.


### -field DVASPECT_THUMBNAIL

Provides a thumbnail representation of an object so it can be displayed in a browsing tool. The thumbnail is approximately a 120 by 120 pixel, 16-color (recommended) device-independent bitmap potentially wrapped in a metafile.


### -field DVASPECT_ICON

Provides an iconic representation of an object.


### -field DVASPECT_DOCPRINT

Provides a representation of the object on the screen as though it were printed to a printer using the <b>Print</b> command from the <b>File</b> menu. The described data may represent a sequence of pages.



## -remarks



Values of this enumeration are used to define the <b>dwAspect</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure. Only one <b>DVASPECT</b> value can be used to specify a single presentation aspect in a <b>FORMATETC</b> structure. The <b>FORMATETC</b> structure is used in many OLE functions and interface methods that require information on data presentation.



The default value of <b>MiscStatus</b> is used if a subkey corresponding to the specified <b>DVASPECT</b> is not found. To set an OLE control, specify DVASPECT==1. This will cause the following to occur in the registry:


<pre xml:space="preserve"><b>HKEY_CLASSES_ROOT\CLSID\ . . .</b>
   <b>MiscStatus</b> = 1</pre>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iviewobject2">IViewObject2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/ns-oleidl-objectdescriptor">OBJECTDESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole/nf-ole-oledraw">OleDraw</a>
 

 

