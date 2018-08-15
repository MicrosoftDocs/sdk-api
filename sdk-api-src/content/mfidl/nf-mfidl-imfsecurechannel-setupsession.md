---
UID: NF:mfidl.IMFSecureChannel.SetupSession
title: IMFSecureChannel::SetupSession
author: windows-sdk-content
description: Passes the encrypted session key to the client.
old-location: mf\imfsecurechannel_setupsession.htm
old-project: medfound
ms.assetid: a4d38056-ea6a-441e-8b77-39ffd316cb5a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFSecureChannel interface [Media Foundation],SetupSession method, IMFSecureChannel.SetupSession, IMFSecureChannel::SetupSession, SetupSession, SetupSession method [Media Foundation], SetupSession method [Media Foundation],IMFSecureChannel interface, a4d38056-ea6a-441e-8b77-39ffd316cb5a, mf.imfsecurechannel_setupsession, mfidl/IMFSecureChannel::SetupSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSecureChannel.SetupSession
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSecureChannel::SetupSession


## -description



Passes the encrypted session key to the client.




## -parameters




### -param pbEncryptedSessionKey [in]

Pointer to a buffer that contains the encrypted session key. This parameter can be <b>NULL</b>.


### -param cbSessionKey [in]

Size of the <i>pbEncryptedSessionKey</i> buffer, in bytes.


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
 




## -see-also




<a href="https://msdn.microsoft.com/063170b8-9483-4acd-9b42-a226e9c38f0e">IMFSecureChannel</a>
 

 

