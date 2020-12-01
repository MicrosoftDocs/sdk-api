---
UID: NS:olectl.tagOCPFIPARAMS
title: OCPFIPARAMS (olectl.h)
description: Contains parameters used to invoke a property sheet dialog box through the OleCreatePropertyFrameIndirect function.
helpviewer_keywords: ["*LPOCPFIPARAMS","LPOCPFIPARAMS","LPOCPFIPARAMS structure pointer [COM]","OCPFIPARAMS","OCPFIPARAMS structure [COM]","_ctrl_OCPFIPARAMS","com.ocpfiparams","olectl/LPOCPFIPARAMS","olectl/OCPFIPARAMS"]
old-location: com\ocpfiparams.htm
tech.root: com
ms.assetid: d65d8239-495c-4eee-bd9c-8e803fd09a06
ms.date: 12/05/2018
ms.keywords: '*LPOCPFIPARAMS, LPOCPFIPARAMS, LPOCPFIPARAMS structure pointer [COM], OCPFIPARAMS, OCPFIPARAMS structure [COM], _ctrl_OCPFIPARAMS, com.ocpfiparams, olectl/LPOCPFIPARAMS, olectl/OCPFIPARAMS'
req.header: olectl.h
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
req.typenames: OCPFIPARAMS, *LPOCPFIPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOCPFIPARAMS
 - olectl/tagOCPFIPARAMS
 - LPOCPFIPARAMS
 - olectl/LPOCPFIPARAMS
 - OCPFIPARAMS
 - olectl/OCPFIPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Olectl.h
api_name:
 - OCPFIPARAMS
---

# OCPFIPARAMS structure


## -description

Contains parameters used to invoke a property sheet dialog box through the <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframeindirect">OleCreatePropertyFrameIndirect</a> function.

## -struct-fields

### -field cbStructSize

The size of the structure, in bytes.

### -field hWndOwner

Handle to the parent window of the resulting property sheet dialog box.

### -field x

Horizontal position for the dialog box relative to <b>hWndOwner</b>, in pixels.

### -field y

Vertical position for the dialog box relative to <b>hWndOwner</b>, in pixels.

### -field lpszCaption

Pointer to an <a href="/windows/desktop/api/wtypesbase/nf-wtypesbase-olestr">OLESTR</a> that contains the caption of the dialog.

### -field cObjects

Number of object pointers passed in <b>lplpUnk</b>.

### -field lplpUnk

Array of <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointers on the objects for which this property sheet is being invoked. The number of elements in the array is specified by <b>cObjects</b>. These pointers are passed to each property page through <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-setobjects">IPropertyPage::SetObjects</a>.

### -field cPages

Number of property pages specified in <b>lpPages</b>.

### -field lpPages

Pointer to an array of size <b>cPages</b> containing the CLSIDs of each property page to display in the property sheet.

### -field lcid

Locale identifier for the property sheet. This value will be returned through <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getlocaleid">IPropertyPageSite::GetLocaleID</a>.

### -field dispidInitialProperty

Property that is highlighted when the dialog box is made visible.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-setobjects">IPropertyPage::SetObjects</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getlocaleid">IPropertyPageSite::GetLocaleID</a>



<a href="/windows/desktop/api/wtypesbase/nf-wtypesbase-olestr">OLESTR</a>



<a href="/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframeindirect">OleCreatePropertyFrameIndirect</a>