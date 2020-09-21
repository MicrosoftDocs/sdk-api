---
UID: NF:tapi3if.ITBasicCallControl.Conference
title: ITBasicCallControl::Conference (tapi3if.h)
description: The Conference method adds a consultation call to the conference in which the current call is a participant. If an associated ITCallHub object does not exist, it is created.
helpviewer_keywords: ["Conference","Conference method [TAPI 2.2]","Conference method [TAPI 2.2]","ITBasicCallControl interface","ITBasicCallControl interface [TAPI 2.2]","Conference method","ITBasicCallControl.Conference","ITBasicCallControl::Conference","_tapi3_itbasiccallcontrol_conference","tapi3.itbasiccallcontrol_conference","tapi3if/ITBasicCallControl::Conference"]
old-location: tapi3\itbasiccallcontrol_conference.htm
tech.root: tapi3
ms.assetid: 73721921-c943-4adc-a2b1-e8c19ec809ac
ms.date: 12/05/2018
ms.keywords: Conference, Conference method [TAPI 2.2], Conference method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Conference method, ITBasicCallControl.Conference, ITBasicCallControl::Conference, _tapi3_itbasiccallcontrol_conference, tapi3.itbasiccallcontrol_conference, tapi3if/ITBasicCallControl::Conference
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITBasicCallControl::Conference
 - tapi3if/ITBasicCallControl::Conference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl.Conference
---

# ITBasicCallControl::Conference


## -description

The 
Conference method adds a consultation call to the conference in which the current call is a participant. If an associated 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> object does not exist, it is created.

## -parameters

### -param pCall [in]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a> interface for the consultation call.

### -param fSync [in]

Indicates whether the call should be conferenced synchronously (VARIANT_TRUE) or asynchronously (VARIANT_FALSE). See 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect">Connect</a> for additional explanation.

## -returns

This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCall</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCall</i> parameter does not point to a valid interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -remarks

Some service providers do not support this operation while streaming is active. The application may need to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-stopsubstream">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">ITStream::StartStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-startsubstream">ITSubStream::StartSubStream</a> following completion of the operation.

The consultation call (<i>pCall</i>) is created by 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>. The connection is completed by calling the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish">Finish</a> method. Please see 
<a href="/windows/desktop/Tapi/create-a-simple-conference">Create a Simple Conference</a> for an example of using this method.

If the consultation call is not in the CONNECTED state when 
Conference is called, TAPI will use the destination address (as specified when the consultation call was first created via 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>) and try to connect at that time. If the original call had a <b>NULL</b> destination address, 
Conference will fail with E_INVALIDARG.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/Tapi/conference-ovr">Conference overview</a>



<a href="/windows/desktop/Tapi/create-a-simple-conference">Create a Simple Conference</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish">Finish</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callhub">ITCallInfo::get_CallHub</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer">Transfer</a>