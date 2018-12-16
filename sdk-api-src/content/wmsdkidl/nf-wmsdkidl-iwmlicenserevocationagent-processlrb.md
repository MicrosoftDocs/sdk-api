---
UID: NF:wmsdkidl.IWMLicenseRevocationAgent.ProcessLRB
title: IWMLicenseRevocationAgent::ProcessLRB
author: windows-sdk-content
description: The ProcessLRB method removes licenses from the license store on the client computer.
old-location: wmformat\iwmlicenserevocationagent_processlrb.htm
tech.root: wmformat
ms.assetid: 185611f8-beef-47b8-a9c2-abcda7651a18
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMLicenseRevocationAgent interface [windows Media Format],ProcessLRB method, IWMLicenseRevocationAgent.ProcessLRB, IWMLicenseRevocationAgent::ProcessLRB, IWMLicenseRevocationAgentProcessLRB, ProcessLRB, ProcessLRB method [windows Media Format], ProcessLRB method [windows Media Format],IWMLicenseRevocationAgent interface, wmformat.iwmlicenserevocationagent_processlrb, wmsdkidl/IWMLicenseRevocationAgent::ProcessLRB
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMLicenseRevocationAgent::ProcessLRB


## -description



The <b>ProcessLRB</b> method removes licenses from the license store on the client computer.




## -parameters




### -param pSignedLRB [in]

Address of the signed license revocation blob in memory. This blob is sent to your application by the license server.


### -param dwSignedLRBLength [in]

Size of the license revocation blob in bytes.


### -param pSignedACK [out]

Address of a buffer that receives the signed acknowledgement of license revocation. Your application must send the acknowledgement to the license server.


### -param pdwSignedACKLength [out]

Size of the acknowledgement in bytes.


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



The license server sends the signed license revocation blob after receiving a response to its initial challenge message. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Dd757226(v=VS.85).aspx">GetLRBChallenge</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757225(v=VS.85).aspx">IWMLicenseRevocationAgent Interface</a>
 

 

