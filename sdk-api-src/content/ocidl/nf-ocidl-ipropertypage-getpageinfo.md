---
UID: NF:ocidl.IPropertyPage.GetPageInfo
title: IPropertyPage::GetPageInfo
author: windows-sdk-content
description: Retrieves information about the property page.
old-location: com\ipropertypage_getpageinfo.htm
tech.root: com
ms.assetid: 3cb7168c-bb05-4e01-a73b-11a52c5e690b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetPageInfo, GetPageInfo method [COM], GetPageInfo method [COM],IPropertyPage interface, IPropertyPage interface [COM],GetPageInfo method, IPropertyPage.GetPageInfo, IPropertyPage::GetPageInfo, _ctrl_ipropertypage_getpageinfo, com.ipropertypage_getpageinfo, ocidl/IPropertyPage::GetPageInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPropertyPage.GetPageInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyPage::GetPageInfo


## -description


Retrieves information about the property page.


## -parameters




### -param pPageInfo [out]

A pointer to the caller-allocated <a href="https://msdn.microsoft.com/363fd45f-fb36-41f0-9d72-dc9c018859ec">PROPPAGEINFO</a> structure in which the property page stores its page information. All allocations stored in this structure become the responsibility of the caller.


## -returns



This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The structure was successfully filled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pPageInfo</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not a valid return value.




## -see-also




<a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>
 

 

