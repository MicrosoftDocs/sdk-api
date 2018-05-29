---
UID: NS:olectl.tagOCPFIPARAMS
title: tagOCPFIPARAMS
author: windows-sdk-content
description: Contains parameters used to invoke a property sheet dialog box through the OleCreatePropertyFrameIndirect function.
old-location: com\ocpfiparams.htm
old-project: com
ms.assetid: d65d8239-495c-4eee-bd9c-8e803fd09a06
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPOCPFIPARAMS, LPOCPFIPARAMS, LPOCPFIPARAMS structure pointer [COM], OCPFIPARAMS, OCPFIPARAMS structure [COM], _ctrl_OCPFIPARAMS, com.ocpfiparams, olectl/LPOCPFIPARAMS, olectl/OCPFIPARAMS, tagOCPFIPARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: OCPFIPARAMS, *LPOCPFIPARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Olectl.h
api_name:
-	OCPFIPARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagOCPFIPARAMS structure


## -description


Contains parameters used to invoke a property sheet dialog box through the <a href="https://msdn.microsoft.com/ccd01d38-2d8e-4509-b44f-fef6ff718558">OleCreatePropertyFrameIndirect</a> function.


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

Pointer to an <a href="https://msdn.microsoft.com/bf3341a0-5b1d-479b-998d-a61bb945e0c3">OLESTR</a> that contains the caption of the dialog.


### -field cObjects

Number of object pointers passed in <b>lplpUnk</b>.


### -field lplpUnk

Array of <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointers on the objects for which this property sheet is being invoked. The number of elements in the array is specified by <b>cObjects</b>. These pointers are passed to each property page through <a href="https://msdn.microsoft.com/0d7a73ce-8e3c-40c5-9040-6370df5edc2b">IPropertyPage::SetObjects</a>.


### -field cPages

Number of property pages specified in <b>lpPages</b>.


### -field lpPages

Pointer to an array of size <b>cPages</b> containing the CLSIDs of each property page to display in the property sheet.


### -field lcid

Locale identifier for the property sheet. This value will be returned through <a href="https://msdn.microsoft.com/d569346d-4a40-42a4-ac8e-539588c4dd66">IPropertyPageSite::GetLocaleID</a>.


### -field dispidInitialProperty

Property that is highlighted when the dialog box is made visible.


## -see-also




<a href="https://msdn.microsoft.com/0d7a73ce-8e3c-40c5-9040-6370df5edc2b">IPropertyPage::SetObjects</a>



<a href="https://msdn.microsoft.com/d569346d-4a40-42a4-ac8e-539588c4dd66">IPropertyPageSite::GetLocaleID</a>



<a href="https://msdn.microsoft.com/bf3341a0-5b1d-479b-998d-a61bb945e0c3">OLESTR</a>



<a href="https://msdn.microsoft.com/ccd01d38-2d8e-4509-b44f-fef6ff718558">OleCreatePropertyFrameIndirect</a>
 

 

