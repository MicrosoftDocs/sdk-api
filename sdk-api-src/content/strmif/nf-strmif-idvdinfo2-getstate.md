---
UID: NF:strmif.IDvdInfo2.GetState
title: IDvdInfo2::GetState
author: windows-sdk-content
description: The GetState method retrieves a bookmark containing the disc location and DVD Navigator state information.
old-location: dshow\idvdinfo2_getstate.htm
tech.root: DirectShow
ms.assetid: 403add2b-3dfd-436d-8184-7a14f30f6ea3
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetState method, IDvdInfo2.GetState, IDvdInfo2::GetState, IDvdInfo2GetState, dshow.idvdinfo2_getstate, strmif/IDvdInfo2::GetState
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo2::GetState


## -description



The <code>GetState</code> method retrieves a bookmark containing the disc location and DVD Navigator state information.




## -parameters




### -param pStateData [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/df30a3b9-7541-42a8-b642-3b6450a0345e">IDvdState</a> interface of a <b>DvdState</b> object allocated by the DVD Navigator.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD Navigator is not initialized.

</td>
</tr>
</table>
 




## -remarks



When this method is called, the DVD Navigator creates a new state object and saves the current location into it, as well as the current parental level and other state information. The <b>DVDState</b> object can be used to restore the DVD Navigator to the saved location at a later time through a call to <a href="https://msdn.microsoft.com/3941b469-46f3-4499-9062-81a873a36292">IDvdControl2::SetState</a>. This enables viewers to stop viewing in the middle of a disc, save the location, and come back at some later time to begin viewing where they left off, with all the internal settings restored as they were before.

The DVD Navigator calls <b>AddRef</b> on the <b>DvdState</b> object before returning it to the application. The application must call <b>Release</b> on the object when it is finished with it.

This method is demonstrated in the DVDSample application in <b>CDvdCore::RestoreBookmark</b>.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

