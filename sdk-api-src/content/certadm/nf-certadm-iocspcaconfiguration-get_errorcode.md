---
UID: NF:certadm.IOCSPCAConfiguration.get_ErrorCode
title: IOCSPCAConfiguration::get_ErrorCode
author: windows-sdk-content
description: Gets a code that identifies an error condition in a CA configuration.
old-location: security\iocspcaconfiguration_errorcode_method.htm
tech.root: seccrypto
ms.assetid: ef41699e-761b-454e-a759-424bb5989459
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ErrorCode property [Security], ErrorCode property [Security],IOCSPCAConfiguration interface, IOCSPCAConfiguration interface [Security],ErrorCode property, IOCSPCAConfiguration.ErrorCode, IOCSPCAConfiguration.get_ErrorCode, IOCSPCAConfiguration::ErrorCode, IOCSPCAConfiguration::get_ErrorCode, certadm/IOCSPCAConfiguration::ErrorCode, certadm/IOCSPCAConfiguration::get_ErrorCode, get_ErrorCode, security.iocspcaconfiguration_errorcode_method
ms.topic: method
req.header: certadm.h
req.include-header: Certserv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPCAConfiguration.ErrorCode
 - IOCSPCAConfiguration.get_ErrorCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCSPCAConfiguration::get_ErrorCode


## -description


The <b>ErrorCode</b> property gets a code that identifies an error condition in a CA configuration. The default implementations of <a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPAdmin</a> and <a href="https://msdn.microsoft.com/4e232c34-b5ab-4269-903b-189aac5a8ddc">IOCSPCAConfigurationCollection</a> set the initial error-condition value.

This property is read-only.


## -parameters


## -remarks



The OCSP responder service returns an error code when it encounters a problem with a configuration. For the definition of a returned code, see Winerror.h in the Microsoft Windows Software Development Kit (SDK).

An <b>OCSPCAConfiguration</b> object internally stores the error code as an <b>HRESULT</b> with an initial value of <b>E_PENDING</b>. When <a href="https://msdn.microsoft.com/973c69c3-282b-4e17-bb44-119965a4b443">IOCSPAdmin::SetConfiguration</a> is called, the error code is reset to <b>E_PENDING</b>.




## -see-also




<a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a>
 

 

