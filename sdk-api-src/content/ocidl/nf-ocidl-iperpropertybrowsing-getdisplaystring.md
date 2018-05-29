---
UID: NF:ocidl.IPerPropertyBrowsing.GetDisplayString
title: IPerPropertyBrowsing::GetDisplayString
author: windows-sdk-content
description: Retrieves a text string describing the specified property.
old-location: com\iperpropertybrowsing_getdisplaystring.htm
old-project: com
ms.assetid: 949d7d12-de59-441d-ac0f-e18f050d005d
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetDisplayString, GetDisplayString method [COM], GetDisplayString method [COM],IPerPropertyBrowsing interface, IPerPropertyBrowsing interface [COM],GetDisplayString method, IPerPropertyBrowsing.GetDisplayString, IPerPropertyBrowsing::GetDisplayString, _ctrl_iperpropertybrowsing_getdisplaystring, com.iperpropertybrowsing_getdisplaystring, ocidl/IPerPropertyBrowsing::GetDisplayString
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IPerPropertyBrowsing.GetDisplayString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPerPropertyBrowsing::GetDisplayString


## -description


Retrieves a text string describing the specified property.


## -parameters




### -param dispID [in]

The dispatch identifier of the property whose display name is requested.


### -param pBstr [out]

A pointer to a variable that receives the display name for the property identified in <i>dispID</i>. The string is allocated by this method using <b>SysAllocString</b>. Upon return, the string is the responsibility of the caller, which must free it with <b>SysFreeString</b> when it is no longer needed.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The display name was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The object does not provide display names for individual properties. The caller has the recourse to check the object's type information for the text name of the object in this case.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in pbstr is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/05e46df3-b6c8-4520-af11-21e1ff90fb9f">IPerPropertyBrowsing</a>
 

 

