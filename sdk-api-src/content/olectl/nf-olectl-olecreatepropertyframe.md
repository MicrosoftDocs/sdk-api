---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# OleCreatePropertyFrame function


## -description


Invokes a new property frame, that is, a property sheet dialog box, whose parent is <i>hwndOwner</i>, where the dialog is positioned at the point (x,y) in the parent window and has the caption <i>lpszCaption</i>.




## -parameters




### -param hwndOwner [in]

Handle to the parent window of the resulting property sheet dialog box.


### -param x [in]

Reserved. Horizontal position for the dialog box relative to <i>hwndOwner</i>.


### -param y [in]

Reserved. Vertical position for the dialog box relative to <i>hwndOwner</i>.


### -param lpszCaption [in]

Pointer to the string used for the caption of the dialog box.


### -param cObjects [in]

Number of object pointers passed in <i>ppUnk</i>.


### -param ppUnk [in]

An array of <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointers on the objects for which this property sheet is being invoked. The number of elements in the array is specified by <i>cObjects</i>. These pointers are passed to each property page through <a href="https://msdn.microsoft.com/0d7a73ce-8e3c-40c5-9040-6370df5edc2b">IPropertyPage::SetObjects</a>.


### -param cPages [in]

Number of property pages specified in <i>pPageCIsID</i>.


### -param pPageClsID [in]

Array of size <i>cPages</i> containing the CLSIDs of each property page to display in the property sheet.


### -param lcid [in]

Locale identifier to use for the property sheet. Property pages can retrieve this identifier through <a href="https://msdn.microsoft.com/d569346d-4a40-42a4-ac8e-539588c4dd66">IPropertyPageSite::GetLocaleID</a>.


### -param dwReserved [in]

Reserved for future use; must be zero.


### -param pvReserved [in]

Reserved for future use; must be <b>NULL</b>.


## -returns



This function supports the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The dialog box was invoked and operated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>lpszCaption</i>, <i>ppUnk</i>, or <i>pPageCIsID</i> is not valid. For example, any one of them may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The property pages to be displayed are identified with <i>pPageClsID</i>, which is an array of <i>cPages</i> <a href="https://msdn.microsoft.com/8f2be90c-360a-410c-81aa-bae9ae2c1a21">CLSID</a> values. The objects that are affected by this property sheet are identified in <i>ppUnk</i>, an array of size <i>cObjects</i> containing <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointers.

This function always creates a modal dialog box and does not return until the dialog box is closed.




## -see-also




<a href="https://msdn.microsoft.com/0d7a73ce-8e3c-40c5-9040-6370df5edc2b">IPropertyPage::SetObjects</a>



<a href="https://msdn.microsoft.com/d569346d-4a40-42a4-ac8e-539588c4dd66">IPropertyPageSite::GetLocaleID</a>
 

 

