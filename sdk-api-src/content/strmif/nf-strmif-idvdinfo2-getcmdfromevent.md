---
UID: NF:strmif.IDvdInfo2.GetCmdFromEvent
title: IDvdInfo2::GetCmdFromEvent
author: windows-sdk-content
description: The GetCmdFromEvent method retrieves an IDvdCmd object from an EC_DVD_CMD_START or EC_DVD_CMD_END event.
old-location: dshow\idvdinfo2_getcmdfromevent.htm
tech.root: DirectShow
ms.assetid: 488a394f-222f-4536-a20a-579df5c2f91f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetCmdFromEvent, GetCmdFromEvent method [DirectShow], GetCmdFromEvent method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCmdFromEvent method, IDvdInfo2.GetCmdFromEvent, IDvdInfo2::GetCmdFromEvent, IDvdInfo2GetCmdFromEvent, dshow.idvdinfo2_getcmdfromevent, strmif/IDvdInfo2::GetCmdFromEvent
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
 - IDvdInfo2.GetCmdFromEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo2::GetCmdFromEvent


## -description



The <code>GetCmdFromEvent</code> method retrieves an <a href="https://msdn.microsoft.com/85f9b208-ddc2-4d9c-a30b-b666c81a49d2">IDvdCmd</a> object from an <a href="https://msdn.microsoft.com/230116b4-23f1-4c37-a781-da2c5aa20a1f">EC_DVD_CMD_START</a> or <a href="https://msdn.microsoft.com/f460db8e-b966-41fa-bfa1-4ad3fa65c3e3">EC_DVD_CMD_END</a> event.




## -parameters




### -param lParam1 [in]

Event notification's <i>lParam1</i> parameter.


### -param pCmdObj

TBD




#### - ppCmdObj [out]

Receives a pointer to the  <a href="https://msdn.microsoft.com/85f9b208-ddc2-4d9c-a30b-b666c81a49d2">IDvdCmd</a> interface that is associated with the command that fired the event.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The command no longer exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -remarks



This method maps the <i>lParam1</i> parameter of an EC_DVD_CMD_START or EC_DVD_CMD_END event into an <a href="https://msdn.microsoft.com/85f9b208-ddc2-4d9c-a30b-b666c81a49d2">IDvdCmd</a> object that is associated with the command that fired the event. You can then call <a href="https://msdn.microsoft.com/7badcc93-b5e7-4f43-bd71-a0b9ddfb0053">WaitForStart</a> or <a href="https://msdn.microsoft.com/e7dc3113-616a-49d5-bcab-7ed5aa520b18">WaitForEnd</a> to control the blocking behavior of the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> with respect to that command. The IDvdCmd object is created by the DVD Navigator and the returned pointer has already had its reference count incremented, so you must release it after <b>WaitForStart</b> or <b>WaitForEnd</b> returns.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>



<a href="https://msdn.microsoft.com/37e8f940-617d-43f6-92bd-aadccafe0059">Synchronizing DVD Commands</a>
 

 

