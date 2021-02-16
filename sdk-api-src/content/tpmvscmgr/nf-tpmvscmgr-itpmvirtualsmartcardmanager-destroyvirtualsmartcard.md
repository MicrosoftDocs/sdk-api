---
UID: NF:tpmvscmgr.ITpmVirtualSmartCardManager.DestroyVirtualSmartCard
title: ITpmVirtualSmartCardManager::DestroyVirtualSmartCard (tpmvscmgr.h)
description: Destroys the TPM virtual smart card that has the given instance ID.
helpviewer_keywords: ["DestroyVirtualSmartCard","DestroyVirtualSmartCard method [Security]","DestroyVirtualSmartCard method [Security]","ITpmVirtualSmartCardManager interface","ITpmVirtualSmartCardManager interface [Security]","DestroyVirtualSmartCard method","ITpmVirtualSmartCardManager.DestroyVirtualSmartCard","ITpmVirtualSmartCardManager::DestroyVirtualSmartCard","security.itpmvirtualsmartcardmanager_destroyvirtualsmartcard","tpmvscmgr/ITpmVirtualSmartCardManager::DestroyVirtualSmartCard"]
old-location: security\itpmvirtualsmartcardmanager_destroyvirtualsmartcard.htm
tech.root: security
ms.assetid: C8624CBF-FC39-4269-9405-8E7B5EE88F8D
ms.date: 12/05/2018
ms.keywords: DestroyVirtualSmartCard, DestroyVirtualSmartCard method [Security], DestroyVirtualSmartCard method [Security],ITpmVirtualSmartCardManager interface, ITpmVirtualSmartCardManager interface [Security],DestroyVirtualSmartCard method, ITpmVirtualSmartCardManager.DestroyVirtualSmartCard, ITpmVirtualSmartCardManager::DestroyVirtualSmartCard, security.itpmvirtualsmartcardmanager_destroyvirtualsmartcard, tpmvscmgr/ITpmVirtualSmartCardManager::DestroyVirtualSmartCard
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
 - ITpmVirtualSmartCardManager::DestroyVirtualSmartCard
 - tpmvscmgr/ITpmVirtualSmartCardManager::DestroyVirtualSmartCard
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
 - ITpmVirtualSmartCardManager.DestroyVirtualSmartCard
---

# ITpmVirtualSmartCardManager::DestroyVirtualSmartCard


## -description

Destroys the TPM virtual smart card that has the given instance ID.

## -parameters

### -param pszInstanceId [in]

Instance identifier of the TPM virtual smart card that is returned from a successful <a href="/windows/desktop/api/tpmvscmgr/nf-tpmvscmgr-itpmvirtualsmartcardmanager-createvirtualsmartcard">CreateVirtualSmartCard</a> method call.

### -param pStatusCallback [in, optional]

Pointer to a <a href="/windows/desktop/api/tpmvscmgr/nn-tpmvscmgr-itpmvirtualsmartcardmanagerstatuscallback">ITpmVirtualSmartCardManagerStatusCallback</a> interface. The TPM virtual smart card manager uses this callback interface to communicate the progress and errors during creation of the virtual smart card. If the <i>pStatusCallback</i> parameter is <b>NULL</b>, no progress is reported to the client before the operation completes.

### -param pfNeedReboot [out]

Pointer to a Boolean value to receive whether the requested operation needs to reboot the client computer.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns a Win32 error code.

## -see-also

<a href="/windows/desktop/api/tpmvscmgr/nn-tpmvscmgr-itpmvirtualsmartcardmanager">ITpmVirtualSmartCardManager</a>