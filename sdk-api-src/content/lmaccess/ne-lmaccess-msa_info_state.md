---
UID: NE:lmaccess._MSA_INFO_STATE
title: MSA_INFO_STATE (lmaccess.h)
description: Indicates the state of a managed service account.
helpviewer_keywords: ["*PMSA_INFO_STATE","MSA_INFO_STATE","MSA_INFO_STATE enumeration [Security]","MsaInfoCanInstall","MsaInfoCannotInstall","MsaInfoInstalled","MsaInfoNotExist","MsaInfoNotService","lmaccess/MSA_INFO_STATE","lmaccess/MsaInfoCanInstall","lmaccess/MsaInfoCannotInstall","lmaccess/MsaInfoInstalled","lmaccess/MsaInfoNotExist","lmaccess/MsaInfoNotService","security.msa_info_state"]
old-location: security\msa_info_state.htm
tech.root: security
ms.assetid: 3cba6c6a-1d63-4795-b009-1fcdf86cc2ef
ms.date: 12/05/2018
ms.keywords: '*PMSA_INFO_STATE, MSA_INFO_STATE, MSA_INFO_STATE enumeration [Security], MsaInfoCanInstall, MsaInfoCannotInstall, MsaInfoInstalled, MsaInfoNotExist, MsaInfoNotService, lmaccess/MSA_INFO_STATE, lmaccess/MsaInfoCanInstall, lmaccess/MsaInfoCannotInstall, lmaccess/MsaInfoInstalled, lmaccess/MsaInfoNotExist, lmaccess/MsaInfoNotService, security.msa_info_state'
req.header: lmaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MSA_INFO_STATE, *PMSA_INFO_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MSA_INFO_STATE
 - lmaccess/_MSA_INFO_STATE
 - PMSA_INFO_STATE
 - lmaccess/PMSA_INFO_STATE
 - MSA_INFO_STATE
 - lmaccess/MSA_INFO_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - MSA_INFO_STATE
---

# MSA_INFO_STATE enumeration


## -description

Indicates the state of a managed service account. A managed service account  can be  either a group managed service account (gMSA) or a standalone managed service account (sMSA). A sMSA is limited to being deployed to a single computer.

## -enum-fields

### -field MsaInfoNotExist:1

The account does not exist.

### -field MsaInfoNotService

The account exists, but it is not a group managed service account (gMSA) or a Windows Server 2008 R2 or Windows 7 managed service account.

<b>Windows Server 2008 R2 and Windows 7:  </b> The account is not a managed service account.

### -field MsaInfoCannotInstall

If the managed service account is a gMSA, the credentials cannot be fetched from the active directory or the Kerberos encryption types did not match.

<b>Windows Server 2008 R2 and Windows 7:  </b> The managed service account cannot be installed.

### -field MsaInfoCanInstall

The sMSA can be installed. This constant will never be returned for a gMSA. 

<b>Windows Server 2008 R2 and Windows 7:  </b> The managed service account can be installed.

### -field MsaInfoInstalled

The gMSA managed service account is installed.

<b>Windows Server 2008 R2 and Windows 7:  </b> The managed service account is installed.

## -remarks

Service accounts  can be group managed and are called group managed service accounts (gMSA). Standalone managed service accounts (sMSA) are limited to being deployed to a single computer.

<b>Windows Server 2008 R2 and Windows 7:  </b> The managed service account (MSA) is limited to being deployed to a single computer.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-msa_info_0">MSA_INFO_0</a>
