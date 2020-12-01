---
UID: NF:casetup.ICertSrvSetup.get_CAErrorString
title: ICertSrvSetup::get_CAErrorString (casetup.h)
description: Gets the string data for additional error information related to a failed certification authority (CA) specification.
helpviewer_keywords: ["CAErrorString property [Security]","CAErrorString property [Security]","ICertSrvSetup interface","ICertSrvSetup interface [Security]","CAErrorString property","ICertSrvSetup.CAErrorString","ICertSrvSetup.get_CAErrorString","ICertSrvSetup::CAErrorString","ICertSrvSetup::get_CAErrorString","casetup/ICertSrvSetup::CAErrorString","casetup/ICertSrvSetup::get_CAErrorString","get_CAErrorString","security.icertsrvsetup_caerrorstring"]
old-location: security\icertsrvsetup_caerrorstring.htm
tech.root: security
ms.assetid: 154397f8-aa0e-4d74-b18e-b68b46fdfcdb
ms.date: 12/05/2018
ms.keywords: CAErrorString property [Security], CAErrorString property [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],CAErrorString property, ICertSrvSetup.CAErrorString, ICertSrvSetup.get_CAErrorString, ICertSrvSetup::CAErrorString, ICertSrvSetup::get_CAErrorString, casetup/ICertSrvSetup::CAErrorString, casetup/ICertSrvSetup::get_CAErrorString, get_CAErrorString, security.icertsrvsetup_caerrorstring
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertSrvSetup::get_CAErrorString
 - casetup/ICertSrvSetup::get_CAErrorString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.CAErrorString
 - ICertSrvSetup.get_CAErrorString
---

# ICertSrvSetup::get_CAErrorString


## -description

The <b>CAErrorString</b> property gets the string data for additional error information related to a failed <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) specification. Any method call on the parent object resets this property.

This property is read-only.

## -parameters

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>