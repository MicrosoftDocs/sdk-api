---
UID: NF:d2d1_1.ID2D1Factory1.GetRegisteredEffects
title: ID2D1Factory1::GetRegisteredEffects
author: windows-sdk-content
description: Returns the class IDs of the currently registered effects and global effects on this factory.
old-location: direct2d\id2d1factory1_getregisteredeffects.htm
tech.root: direct2d
ms.assetid: c3363411-908f-4b02-b77e-ca563094f9a5
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetRegisteredEffects, GetRegisteredEffects method [Direct2D], GetRegisteredEffects method [Direct2D],ID2D1Factory1 interface, ID2D1Factory1 interface [Direct2D],GetRegisteredEffects method, ID2D1Factory1.GetRegisteredEffects, ID2D1Factory1::GetRegisteredEffects, d2d1_1/ID2D1Factory1::GetRegisteredEffects, direct2d.id2d1factory1_getregisteredeffects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory1.GetRegisteredEffects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory1::GetRegisteredEffects


## -description


Returns the class IDs of the currently registered effects and global effects on this factory.


## -parameters




### -param effects [out]

Type: <b><a href="https://msdn.microsoft.com/8f2be90c-360a-410c-81aa-bae9ae2c1a21">CLSID</a>*</b>

When this method returns, contains an array of effects. <b>NULL</b> if no effects are retrieved.


### -param effectsCount

TBD


### -param effectsReturned [out]

Type: <b><a href="https://msdn.microsoft.com/dcb864f2-f162-41ca-b3ef-5b592a311299">UINT32</a>*</b>

When this method returns, contains the  number of effects copied into <i>effects</i>.


### -param effectsRegistered [out, optional]

Type: <b><a href="https://msdn.microsoft.com/dcb864f2-f162-41ca-b3ef-5b592a311299">UINT32</a>*</b>

When this method returns, contains the number of effects currently registered in the system.


#### - effectCount

Type: <b><a href="https://msdn.microsoft.com/dcb864f2-f162-41ca-b3ef-5b592a311299">UINT32</a></b>

The capacity of the <i>effects</i> array.


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</td>
<td><i>effectsRegistered</i> is larger than <i>effectCount</i>.</td>
</tr>
</table>
 




## -remarks



The set of class IDs will be atomically returned by the API. The set will not be interrupted by other threads registering or unregistering effects.

If <i>effectsRegistered</i> is larger than <i>effectCount</i>, the supplied array will still be filled to capacity with the current set of registered effects. This method returns the CLSIDs for all global effects and all effects registered to this factory.




## -see-also




<a href="https://msdn.microsoft.com/8221c3b4-e331-403c-9406-ee8d3e103825">ID2D1Factory1</a>



<a href="https://msdn.microsoft.com/9988aad6-0487-4f48-a05c-1dfb944f6ce7">ID2D1Factory1::RegisterEffect</a>
 

 

