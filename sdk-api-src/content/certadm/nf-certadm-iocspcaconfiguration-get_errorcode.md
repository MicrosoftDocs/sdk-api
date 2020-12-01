---
UID: NF:certadm.IOCSPCAConfiguration.get_ErrorCode
title: IOCSPCAConfiguration::get_ErrorCode (certadm.h)
description: Gets a code that identifies an error condition in a CA configuration.
helpviewer_keywords: ["ErrorCode property [Security]","ErrorCode property [Security]","IOCSPCAConfiguration interface","IOCSPCAConfiguration interface [Security]","ErrorCode property","IOCSPCAConfiguration.ErrorCode","IOCSPCAConfiguration.get_ErrorCode","IOCSPCAConfiguration::ErrorCode","IOCSPCAConfiguration::get_ErrorCode","certadm/IOCSPCAConfiguration::ErrorCode","certadm/IOCSPCAConfiguration::get_ErrorCode","get_ErrorCode","security.iocspcaconfiguration_errorcode_method"]
old-location: security\iocspcaconfiguration_errorcode_method.htm
tech.root: security
ms.assetid: ef41699e-761b-454e-a759-424bb5989459
ms.date: 12/05/2018
ms.keywords: ErrorCode property [Security], ErrorCode property [Security],IOCSPCAConfiguration interface, IOCSPCAConfiguration interface [Security],ErrorCode property, IOCSPCAConfiguration.ErrorCode, IOCSPCAConfiguration.get_ErrorCode, IOCSPCAConfiguration::ErrorCode, IOCSPCAConfiguration::get_ErrorCode, certadm/IOCSPCAConfiguration::ErrorCode, certadm/IOCSPCAConfiguration::get_ErrorCode, get_ErrorCode, security.iocspcaconfiguration_errorcode_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPCAConfiguration::get_ErrorCode
 - certadm/IOCSPCAConfiguration::get_ErrorCode
dev_langs:
 - c++
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
---

# IOCSPCAConfiguration::get_ErrorCode


## -description

The <b>ErrorCode</b> property gets a code that identifies an error condition in a CA configuration. The default implementations of <a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a> and <a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfigurationcollection">IOCSPCAConfigurationCollection</a> set the initial error-condition value.

This property is read-only.

## -parameters

## -remarks

The OCSP responder service returns an error code when it encounters a problem with a configuration. For the definition of a returned code, see Winerror.h in the Microsoft Windows Software Development Kit (SDK).

An <b>OCSPCAConfiguration</b> object internally stores the error code as an <b>HRESULT</b> with an initial value of <b>E_PENDING</b>. When <a href="/windows/desktop/api/certadm/nf-certadm-iocspadmin-setconfiguration">IOCSPAdmin::SetConfiguration</a> is called, the error code is reset to <b>E_PENDING</b>.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>