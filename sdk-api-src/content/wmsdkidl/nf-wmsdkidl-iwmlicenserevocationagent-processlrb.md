---
UID: NF:wmsdkidl.IWMLicenseRevocationAgent.ProcessLRB
title: IWMLicenseRevocationAgent::ProcessLRB (wmsdkidl.h)
description: The ProcessLRB method removes licenses from the license store on the client computer.
helpviewer_keywords: ["IWMLicenseRevocationAgent interface [windows Media Format]","ProcessLRB method","IWMLicenseRevocationAgent.ProcessLRB","IWMLicenseRevocationAgent::ProcessLRB","IWMLicenseRevocationAgentProcessLRB","ProcessLRB","ProcessLRB method [windows Media Format]","ProcessLRB method [windows Media Format]","IWMLicenseRevocationAgent interface","wmformat.iwmlicenserevocationagent_processlrb","wmsdkidl/IWMLicenseRevocationAgent::ProcessLRB"]
old-location: wmformat\iwmlicenserevocationagent_processlrb.htm
tech.root: wmformat
ms.assetid: 185611f8-beef-47b8-a9c2-abcda7651a18
ms.date: 4/26/2023
ms.keywords: IWMLicenseRevocationAgent interface [windows Media Format],ProcessLRB method, IWMLicenseRevocationAgent.ProcessLRB, IWMLicenseRevocationAgent::ProcessLRB, IWMLicenseRevocationAgentProcessLRB, ProcessLRB, ProcessLRB method [windows Media Format], ProcessLRB method [windows Media Format],IWMLicenseRevocationAgent interface, wmformat.iwmlicenserevocationagent_processlrb, wmsdkidl/IWMLicenseRevocationAgent::ProcessLRB
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMLicenseRevocationAgent::ProcessLRB
 - wmsdkidl/IWMLicenseRevocationAgent::ProcessLRB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMLicenseRevocationAgent.ProcessLRB
---

# IWMLicenseRevocationAgent::ProcessLRB


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>ProcessLRB</b> method removes licenses from the license store on the client computer.

## -parameters

### -param pSignedLRB [in]

Address of the signed license revocation blob in memory. This blob is sent to your application by the license server.

### -param dwSignedLRBLength [in]

Size of the license revocation blob in bytes.

### -param pSignedACK [out]

Address of a buffer that receives the signed acknowledgment of license revocation. Your application must send the acknowledgment to the license server.

### -param pdwSignedACKLength [out]

Size of the acknowledgment in bytes.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

The license server sends the signed license revocation blob after receiving a response to its initial challenge message. For more information, see <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge">GetLRBChallenge</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent">IWMLicenseRevocationAgent Interface</a>