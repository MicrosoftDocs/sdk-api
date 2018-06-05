---
UID: NF:strmif.IDvdInfo2.GetCurrentLocation
title: IDvdInfo2::GetCurrentLocation
author: windows-sdk-content
description: The GetCurrentLocation method retrieves the current playback location.
old-location: dshow\idvdinfo2_getcurrentlocation.htm
old-project: DirectShow
ms.assetid: 54005c07-1689-411c-88a9-bcd19cc065dd
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetCurrentLocation, GetCurrentLocation method [DirectShow], GetCurrentLocation method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentLocation method, IDvdInfo2.GetCurrentLocation, IDvdInfo2::GetCurrentLocation, IDvdInfo2GetCurrentLocation, dshow.idvdinfo2_getcurrentlocation, strmif/IDvdInfo2::GetCurrentLocation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdInfo2.GetCurrentLocation
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetCurrentLocation


## -description



The <code>GetCurrentLocation</code> method retrieves the current playback location.




## -parameters




### -param pLocation [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/58506709-42e2-43e4-a4c7-b522b7d06e6f">DVD_PLAYBACK_LOCATION2</a> that receives the playback location information.


## -returns



Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pLocation</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is in an invalid domain.

</td>
</tr>
</table>
 




## -remarks



This method retrieves information sufficient to restart playback of a video from the current playback location in titles that don't explicitly disable seeking to the current location. After the disc has been ejected, the information returned by this method will not necessarily be sufficient to restart playback. To save the current location and state information to disc so that the user can return to the same location at any later time, use <a href="https://msdn.microsoft.com/403add2b-3dfd-436d-8184-7a14f30f6ea3">GetState</a>.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

