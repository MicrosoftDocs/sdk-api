---
UID: NE:oleidl.tagOLERENDER
title: OLERENDER (oleidl.h)
description: Indicates the type of caching requested for newly created objects.
helpviewer_keywords: ["*LPOLERENDER","LPOLERENDER","LPOLERENDER enumeration pointer [COM]","OLERENDER","OLERENDER enumeration [COM]","OLERENDER_ASIS","OLERENDER_DRAW","OLERENDER_FORMAT","OLERENDER_NONE","_ole_OLERENDER","com.olerender","oleidl/LPOLERENDER","oleidl/OLERENDER","oleidl/OLERENDER_ASIS","oleidl/OLERENDER_DRAW","oleidl/OLERENDER_FORMAT","oleidl/OLERENDER_NONE"]
old-location: com\olerender.htm
tech.root: com
ms.assetid: bab871ba-4ec4-49fd-854a-585732b91290
ms.date: 12/05/2018
ms.keywords: '*LPOLERENDER, LPOLERENDER, LPOLERENDER enumeration pointer [COM], OLERENDER, OLERENDER enumeration [COM], OLERENDER_ASIS, OLERENDER_DRAW, OLERENDER_FORMAT, OLERENDER_NONE, _ole_OLERENDER, com.olerender, oleidl/LPOLERENDER, oleidl/OLERENDER, oleidl/OLERENDER_ASIS, oleidl/OLERENDER_DRAW, oleidl/OLERENDER_FORMAT, oleidl/OLERENDER_NONE'
req.header: oleidl.h
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
targetos: Windows
req.typenames: OLERENDER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLERENDER
 - oleidl/tagOLERENDER
 - OLERENDER
 - oleidl/OLERENDER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLERENDER
---

# OLERENDER enumeration


## -description

Indicates the type of caching requested for newly created objects.

## -enum-fields

### -field OLERENDER_NONE:0

The client is not requesting any locally cached drawing or data retrieval capabilities in the object. The <i>pFormatEtc</i> parameter of the calls is ignored when this value is specified for the <i>renderopts</i> parameter.

### -field OLERENDER_DRAW:1

The client will draw the content of the object on the screen (a <b>NULL</b> target device) using <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a>. The object itself determines the data formats that need to be cached. With this render option, only the <b>ptd</b> and <b>dwAspect</b> members of <i>pFormatEtc</i> are significant, since the object may cache things differently depending on the parameter values. However, <i>pFormatEtc</i> can legally be <b>NULL</b> here, in which case the object is to assume the display target device and the DVASPECT_CONTENT aspect.

### -field OLERENDER_FORMAT:2

The client will pull one format from the object using <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>. The format of the data to be cached is passed in <i>pFormatEtc</i>, which may not in this case be <b>NULL</b>.

### -field OLERENDER_ASIS:3

The client is not requesting any locally cached drawing or data retrieval capabilities in the object. <i>pFormatEtc</i> is ignored for this option. The difference between this and the OLERENDER_FORMAT value is important in such functions as <a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a> and <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinkfromdata">OleCreateLinkFromData</a>.

## -see-also

<a href="/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a>



<a href="/windows/desktop/api/ole/nf-ole-olecreatefromfile">OleCreateFromFile</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatelink">OleCreateLink</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinkfromdata">OleCreateLinkFromData</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatelinktofile">OleCreateLinkToFile</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatestaticfromdata">OleCreateStaticFromData</a>
