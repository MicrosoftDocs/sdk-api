---
UID: NF:strmif.IAMExtTransport.GetEditPropertySet
title: IAMExtTransport::GetEditPropertySet
author: windows-sdk-content
description: The GetEditPropertySet method retrieves the state of an edit event.
old-location: dshow\iamexttransport_geteditpropertyset.htm
old-project: DirectShow
ms.assetid: 1afb45da-947c-454d-8be9-46ac58802b9e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetEditPropertySet, GetEditPropertySet method [DirectShow], GetEditPropertySet method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetEditPropertySet method, IAMExtTransport.GetEditPropertySet, IAMExtTransport::GetEditPropertySet, IAMExtTransportGetEditPropertySet, dshow.iamexttransport_geteditpropertyset, strmif/IAMExtTransport::GetEditPropertySet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMExtTransport.GetEditPropertySet
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport::GetEditPropertySet


## -description



The <code>GetEditPropertySet</code> method retrieves the state of an edit event.



This method is not implemented.


## -parameters




### -param EditID [in]

Specifies the edit property set. Use the identifier returned by the <a href="https://msdn.microsoft.com/40695c7c-7381-44c0-b41f-7c838c9c83b5">IAMExtTransport::SetEditPropertySet</a> method.


### -param pState [out]

Pointer to a <b>long</b> integer that receives the state of the edit property set:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>ED_ACTIVE</td>
<td>The edit property set is active.</td>
</tr>
<tr>
<td>ED_DELETE</td>
<td>The edit property set was deleted.</td>
</tr>
<tr>
<td>ED_INACTIVE</td>
<td>The edit property set is inactive.</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/40695c7c-7381-44c0-b41f-7c838c9c83b5">IAMExtTransport::SetEditPropertySet</a>
 

 

