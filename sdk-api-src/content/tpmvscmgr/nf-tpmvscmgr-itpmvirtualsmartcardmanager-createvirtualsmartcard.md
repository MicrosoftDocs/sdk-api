---
UID: NF:tpmvscmgr.ITpmVirtualSmartCardManager.CreateVirtualSmartCard
title: ITpmVirtualSmartCardManager::CreateVirtualSmartCard (tpmvscmgr.h)
description: Creates a TPM virtual smart card with the given parameters.
helpviewer_keywords: ["CreateVirtualSmartCard","CreateVirtualSmartCard method [Security]","CreateVirtualSmartCard method [Security]","ITpmVirtualSmartCardManager interface","ITpmVirtualSmartCardManager interface [Security]","CreateVirtualSmartCard method","ITpmVirtualSmartCardManager.CreateVirtualSmartCard","ITpmVirtualSmartCardManager::CreateVirtualSmartCard","security.itpmvirtualsmartcardmanager_createvirtualsmartcard","tpmvscmgr/ITpmVirtualSmartCardManager::CreateVirtualSmartCard"]
old-location: security\itpmvirtualsmartcardmanager_createvirtualsmartcard.htm
tech.root: security
ms.assetid: C80C4DE2-0C43-40A5-81E6-7036A0B8DEB7
ms.date: 12/05/2018
ms.keywords: CreateVirtualSmartCard, CreateVirtualSmartCard method [Security], CreateVirtualSmartCard method [Security],ITpmVirtualSmartCardManager interface, ITpmVirtualSmartCardManager interface [Security],CreateVirtualSmartCard method, ITpmVirtualSmartCardManager.CreateVirtualSmartCard, ITpmVirtualSmartCardManager::CreateVirtualSmartCard, security.itpmvirtualsmartcardmanager_createvirtualsmartcard, tpmvscmgr/ITpmVirtualSmartCardManager::CreateVirtualSmartCard
req.header: tpmvscmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tpmvscmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vscmgr.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITpmVirtualSmartCardManager::CreateVirtualSmartCard
 - tpmvscmgr/ITpmVirtualSmartCardManager::CreateVirtualSmartCard
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vscmgr.lib
 - Vscmgr.dll
api_name:
 - ITpmVirtualSmartCardManager.CreateVirtualSmartCard
---

# ITpmVirtualSmartCardManager::CreateVirtualSmartCard


## -description

Creates a TPM virtual smart card with the given parameters.

## -parameters

### -param pszFriendlyName [in]

Display name of the smart card reader node. This is shown in the Device Manager, but it is not the reader name as seen by the smart card resource manager (SCRM).

### -param bAdminAlgId [in]

Algorithm identifier of the admin key. Currently, to work with the inbox GIDS minidriver, this value should be VSC_DEFAULT_ADMIN_ALGORITHM_ID (3-key triple DES with ISO/IEC 9797 padding method 2 in CBC chaining mode).

### -param pbAdminKey [in]

Pointer to a byte array that contains the admin key of the virtual smart card to be created.

### -param cbAdminKey [in]

Size, in bytes, of the byte array pointed to by the <i>pbAdminKey</i> parameter.

### -param pbAdminKcv [in, optional]

Pointer to a byte array that contains the key check value of the admin key. Key check value is defined as the first 3 bytes of the output BLOB when using the admin key to encrypt a block of zeros. If the key check value is not provided, there will be no integrity check for the admin key.

### -param cbAdminKcv [in]

Size, in bytes, of the byte array pointed to by the <i>pbAdminKcv</i> parameter.

### -param pbPuk [in, optional]

Pointer to a byte array that contains the PIN unlock key (PUK) value of the virtual smart card. It is usually a sequence of ASCII characters with a minimal length of 8 characters. If the PUK is not provided, the virtual smart card will be created without a PUK role and instead will use the challenge/response-based PIN reset through the admin role.

### -param cbPuk [in]

Size, in bytes, of the byte array pointed to by the <i>pbPuk</i> parameter.

### -param pbPin [in]

Pointer to a byte array that contains the PIN value of the virtual smart card. It is usually a sequence of ASCII characters with a length of 8 characters minimum and 127 characters maximum.

### -param cbPin [in]

Size, in bytes, of the byte array pointed to by the <i>pbPin</i> parameter.

### -param fGenerate [in]

Indicates whether the virtual smart card needs to be provisioned with all necessary files required by the base CSP and smart card KSP.

### -param pStatusCallback [in, optional]

Pointer to a <a href="/windows/desktop/api/tpmvscmgr/nn-tpmvscmgr-itpmvirtualsmartcardmanagerstatuscallback">ITpmVirtualSmartCardManagerStatusCallback</a> interface. The TPM virtual smart card manager uses this callback interface to communicate the progress or error during virtual smart card creation. If the <i>pStatusCallback</i> parameter is <b>NULL</b>, no progress is reported to the client before the operation completes.

### -param ppszInstanceId [out]

Pointer to a pointer to a Unicode buffer to receive the instance ID of the created virtual smart card.

### -param pfNeedReboot [out]

Pointer to a Boolean value to receive whether the requested operation needs to reboot the computer.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns a Win32 error code.

## -remarks

When the method succeeds, the <i>ppszInstanceId</i> parameter points to the Unicode buffer that contains the instance identifier of the newly created TPM virtual smart card reader. When you have finished using the buffer, the caller needs to free the buffer on the client by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function, as directed in the COM memory management rules.

## -see-also

<a href="/windows/desktop/api/tpmvscmgr/nn-tpmvscmgr-itpmvirtualsmartcardmanager">ITpmVirtualSmartCardManager</a>