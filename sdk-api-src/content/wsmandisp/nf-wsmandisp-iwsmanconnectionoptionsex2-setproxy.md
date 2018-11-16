---
UID: NF:wsmandisp.IWSManConnectionOptionsEx2.SetProxy
title: IWSManConnectionOptionsEx2::SetProxy
author: windows-sdk-content
description: Sets the proxy information for the session.
old-location: winrm\iwsmanconnectionoptionsex2_setproxy.htm
tech.root: WinRM
ms.assetid: b87d5625-c77d-41cb-a75d-a45ba0d3fbe6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWSManConnectionOptionsEx2 interface [Windows Remote Management],SetProxy method, IWSManConnectionOptionsEx2.SetProxy, IWSManConnectionOptionsEx2::SetProxy, SetProxy, SetProxy method [Windows Remote Management], SetProxy method [Windows Remote Management],IWSManConnectionOptionsEx2 interface, winrm.iwsmanconnectionoptionsex2_setproxy, wsmandisp/IWSManConnectionOptionsEx2::SetProxy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSManDisp.h
api_name:
 - IWSManConnectionOptionsEx2.SetProxy
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
- apiref
: 
- COM
: 
- wsmandisp.h
: 
- IWSManConnectionOptionsEx2.SetProxy
: 
---

# IWSManConnectionOptionsEx2::SetProxy


## -description


Sets the proxy information for the session.


## -parameters




### -param accessType [in]

Specifies the proxy access type. This parameter must be set to one of the values in the <a href="https://msdn.microsoft.com/c17c3600-6a19-4937-90ff-1a4f7cf5b123">WSManProxyAccessTypeFlags</a> enumeration. The default value is <b>WSManProxyWinHttpConfig</b>.


### -param authenticationMechanism [in]

Specifies the authentication mechanism to use for the proxy.  This parameter is optional and the default value is 0. If this parameter is set to 0, the WinRM client chooses either Kerberos or Negotiate. Otherwise, this parameter must be set to one of the values in the <a href="https://msdn.microsoft.com/4a86dfae-18c9-4865-8b8b-bb0ac01f558c">WSManProxyAuthenticationFlags</a> enumeration. The default value from the enumeration is <b>WSManFlagProxyAuthenticationUseNegotiate</b>.


### -param userName [in]

Specifies the user name for proxy authentication. This parameter is optional. If a value is not specified for this parameter, the default credentials are used.


### -param password [in]

Specifies the password for proxy authentication. This parameter is optional. If a value is not specified for this parameter, the default credentials are used.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The default credentials are the credentials under which the current thread is operating.




## -see-also




<a href="https://msdn.microsoft.com/09159904-0160-411d-af54-f6aca94d4d7d">IWSManConnectionOptionsEx2</a>
 

 

