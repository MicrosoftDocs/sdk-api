---
UID: NL:vsbackup.IVssBackupComponentsEx
title: IVssBackupComponentsEx (vsbackup.h)
description: Provides methods for requesters to run backup and restore operations using multiple writer instances.
helpviewer_keywords: ["IVssBackupComponentsEx","IVssBackupComponentsEx interface [VSS]","IVssBackupComponentsEx interface [VSS]","described","base.ivssbackupcomponentsex","vsbackup/IVssBackupComponentsEx"]
old-location: base\ivssbackupcomponentsex.htm
tech.root: base
ms.assetid: d3a265ab-39cc-4861-9191-9ecf094d8826
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx, IVssBackupComponentsEx interface [VSS], IVssBackupComponentsEx interface [VSS],described, base.ivssbackupcomponentsex, vsbackup/IVssBackupComponentsEx
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponentsEx
 - vsbackup/IVssBackupComponentsEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssBackupComponentsEx
---

# IVssBackupComponentsEx class


## -description

The <b>IVssBackupComponentsEx</b> interface provides methods for requesters to run backup and restore operations using multiple writer instances.

To obtain an instance of the <b>IVssBackupComponentsEx</b> 
   interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> interface, passing 
   <b>IID_IVssBackupComponentsEx</b> as the interface identifier (IID) parameter.

## -inheritance

The <b>IVssBackupComponentsEx</b> interface inherits from <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>. <b>IVssBackupComponentsEx</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>
