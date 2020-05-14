---
UID: NF:strmif.IDvdInfo2.GetCmdFromEvent
title: IDvdInfo2::GetCmdFromEvent (strmif.h)
description: The GetCmdFromEvent method retrieves an IDvdCmd object from an EC_DVD_CMD_START or EC_DVD_CMD_END event.helpviewer_keywords: ["GetCmdFromEvent","GetCmdFromEvent method [DirectShow]","GetCmdFromEvent method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetCmdFromEvent method","IDvdInfo2.GetCmdFromEvent","IDvdInfo2::GetCmdFromEvent","IDvdInfo2GetCmdFromEvent","dshow.idvdinfo2_getcmdfromevent","strmif/IDvdInfo2::GetCmdFromEvent"]
old-location: dshow\idvdinfo2_getcmdfromevent.htm
tech.root: DirectShow
ms.assetid: 488a394f-222f-4536-a20a-579df5c2f91f
ms.date: 12/05/2018
ms.keywords: GetCmdFromEvent, GetCmdFromEvent method [DirectShow], GetCmdFromEvent method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCmdFromEvent method, IDvdInfo2.GetCmdFromEvent, IDvdInfo2::GetCmdFromEvent, IDvdInfo2GetCmdFromEvent, dshow.idvdinfo2_getcmdfromevent, strmif/IDvdInfo2::GetCmdFromEvent
f1_keywords:
- strmif/IDvdInfo2.GetCmdFromEvent
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo2::GetCmdFromEvent


## -description



The <code>GetCmdFromEvent</code> method retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object from an <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-dvd-cmd-start">EC_DVD_CMD_START</a> or <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-dvd-cmd-end">EC_DVD_CMD_END</a> event.




## -parameters




### -param lParam1 [in]

Event notification's <i>lParam1</i> parameter.


### -param pCmdObj [out]

Receives a pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> interface that is associated with the command that fired the event.


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



This method maps the <i>lParam1</i> parameter of an EC_DVD_CMD_START or EC_DVD_CMD_END event into an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that is associated with the command that fired the event. You can then call <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcmd-waitforstart">WaitForStart</a> or <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcmd-waitforend">WaitForEnd</a> to control the blocking behavior of the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> with respect to that command. The IDvdCmd object is created by the DVD Navigator and the returned pointer has already had its reference count incremented, so you must release it after <b>WaitForStart</b> or <b>WaitForEnd</b> returns.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>
 

 

