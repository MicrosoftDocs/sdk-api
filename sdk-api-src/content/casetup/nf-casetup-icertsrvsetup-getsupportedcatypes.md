---
UID: NF:casetup.ICertSrvSetup.GetSupportedCATypes
title: ICertSrvSetup::GetSupportedCATypes (casetup.h)
description: Gets the types of certification authorities (CAs) that can be installed on a computer under the caller context.
helpviewer_keywords: ["GetSupportedCATypes","GetSupportedCATypes method [Security]","GetSupportedCATypes method [Security]","ICertSrvSetup interface","ICertSrvSetup interface [Security]","GetSupportedCATypes method","ICertSrvSetup.GetSupportedCATypes","ICertSrvSetup::GetSupportedCATypes","casetup/ICertSrvSetup::GetSupportedCATypes","security.icertsrvsetup_getsupportedcatypes"]
old-location: security\icertsrvsetup_getsupportedcatypes.htm
tech.root: security
ms.assetid: 404e5c34-f614-4555-9062-c28d4aac5c4b
ms.date: 12/05/2018
ms.keywords: GetSupportedCATypes, GetSupportedCATypes method [Security], GetSupportedCATypes method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetSupportedCATypes method, ICertSrvSetup.GetSupportedCATypes, ICertSrvSetup::GetSupportedCATypes, casetup/ICertSrvSetup::GetSupportedCATypes, security.icertsrvsetup_getsupportedcatypes
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
 - ICertSrvSetup::GetSupportedCATypes
 - casetup/ICertSrvSetup::GetSupportedCATypes
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
 - ICertSrvSetup.GetSupportedCATypes
---

# ICertSrvSetup::GetSupportedCATypes


## -description

The <b>GetSupportedCATypes</b> method gets the types of <a href="/windows/desktop/SecGloss/c-gly">certification authorities</a> (CAs) that can be installed on a computer under the caller context. This method does not change the state of the <b>CCertSrvSetup</b> object.

## -parameters

### -param pCATypes [out]

A pointer to a <b>VARIANT</b> array of <b>VT_UI4</b> types that specify the supported CAs. The <a href="/windows/desktop/api/certsrv/ne-certsrv-enum_catypes">ENUM_CATYPES</a> enumeration specifies the possible values for the array.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>