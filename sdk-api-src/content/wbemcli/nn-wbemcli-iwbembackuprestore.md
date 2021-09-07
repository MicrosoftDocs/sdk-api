---
UID: NN:wbemcli.IWbemBackupRestore
title: IWbemBackupRestore (wbemcli.h)
description: The IWbemBackupRestore interface backs up and restores the contents of the WMI repository.
helpviewer_keywords: ["IWbemBackupRestore","IWbemBackupRestore interface [Windows Management Instrumentation]","IWbemBackupRestore interface [Windows Management Instrumentation]","described","WbemBackupRestore","_hmm_iwbembackuprestore","wbemcli/IWbemBackupRestore","wmi.iwbembackuprestore"]
old-location: wmi\iwbembackuprestore.htm
tech.root: wmi
ms.assetid: 27599145-417b-4ca8-8e25-5fffb2e7008c
ms.date: 12/05/2018
ms.keywords: IWbemBackupRestore, IWbemBackupRestore interface [Windows Management Instrumentation], IWbemBackupRestore interface [Windows Management Instrumentation],described, WbemBackupRestore, _hmm_iwbembackuprestore, wbemcli/IWbemBackupRestore, wmi.iwbembackuprestore
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemBackupRestore
 - wbemcli/IWbemBackupRestore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemBackupRestore
 - WbemBackupRestore
---

# IWbemBackupRestore interface


## -description

The 
<b>IWbemBackupRestore</b> interface backs up and restores the contents of the WMI repository. The affected content of the repository is static data, such as the class definitions that are compiled into the repository when a MOF file is loaded. The dynamic data supplied through providers is not included.

## -inheritance

The <b>IWbemBackupRestore</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemBackupRestore</b> also has these types of members:

## -remarks

The default mode is the same as setting the force mode flag, which breaks all active connections. This results in remote procedure call (RPC) errors from any active COM connections to WMI until new connections are established.

There can be no active connections to the repository during a restore operation. For this reason, the restore operation fails if default parameters are used and there are active connections. A flag can be specified to break all active connections.

<div class="alert"><b>Note</b>  The client making the call must have the proper privilege enabled. Backup requires the <b>SE_RESTORE_NAME</b> privilege, while restoration requires <b>SE_RESTORE_NAME</b>. To enable a privilege, a client application must be running under a user account that has that privilege,  and the privilege must be enabled using the Windows <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function.</div>
<div> </div>
For computers running Windows, any local user can make these calls,  but remote users must have the <b>WBEM_FULL_WRITE_REP</b> access right to the root namespace.

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for
    WMI</a>
