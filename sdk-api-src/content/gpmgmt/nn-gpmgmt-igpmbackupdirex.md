---
UID: NN:gpmgmt.IGPMBackupDirEx
title: IGPMBackupDirEx (gpmgmt.h)
description: The IGPMBackupDirEx interface supports methods that allow you to query GPMBackup, GPMBackupCollection, GPMStarterGPOBackup, and GPMStarterGPOBackupCollection objects when you are using the Group Policy Management Console (GPMC) interfaces.
helpviewer_keywords: ["GPMBackupDirEx","IGPMBackupDirEx","IGPMBackupDirEx interface [GPMC]","IGPMBackupDirEx interface [GPMC]","described","gpmc.igpmbackupdirex","gpmgmt/IGPMBackupDirEx"]
old-location: gpmc\igpmbackupdirex.htm
tech.root: gpmc
ms.assetid: 3008e70c-cc34-45b0-bdfc-17f2e9cd5de0
ms.date: 12/05/2018
ms.keywords: GPMBackupDirEx, IGPMBackupDirEx, IGPMBackupDirEx interface [GPMC], IGPMBackupDirEx interface [GPMC],described, gpmc.igpmbackupdirex, gpmgmt/IGPMBackupDirEx
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMBackupDirEx
 - gpmgmt/IGPMBackupDirEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMBackupDirEx
 - GPMBackupDirEx
---

# IGPMBackupDirEx interface


## -description

The 
<b>IGPMBackupDirEx</b> interface supports methods that allow you to query 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a>,  
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">GPMBackupCollection</a>, <b>GPMStarterGPOBackup</b>,  
and <b>GPMStarterGPOBackupCollection</b>    objects when you are using the Group Policy Management Console (GPMC) interfaces.

To create a <b>GPMBackupDirEx</b> object, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getbackupdir">IGPM2::GetBackupDirEx</a> method.

## -inheritance

The <b>IGPMBackupDirEx</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMBackupDirEx</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM2</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<b>IGPMStarterGPOBackup</b>



<b>IGPMStarterGPOBackupCollection</b>
