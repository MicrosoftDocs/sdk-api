---
UID: NL:vsbackup.IVssBackupComponentsEx2
title: IVssBackupComponentsEx2 (vsbackup.h)
description: Defines additional methods that requesters can use to run backup and restore operations.
helpviewer_keywords: ["IVssBackupComponentsEx2","IVssBackupComponentsEx2 interface","IVssBackupComponentsEx2 interface","described","base.ivssbackupcomponentsex2","vsbackup/IVssBackupComponentsEx2"]
old-location: base\ivssbackupcomponentsex2.htm
tech.root: base
ms.assetid: 69d4d500-0e21-48bd-b90b-d06c88fde136
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx2, IVssBackupComponentsEx2 interface, IVssBackupComponentsEx2 interface,described, base.ivssbackupcomponentsex2, vsbackup/IVssBackupComponentsEx2
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponentsEx2
 - vsbackup/IVssBackupComponentsEx2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsBackup.h
api_name:
 - IVssBackupComponentsEx2
---

# IVssBackupComponentsEx2 class


## -description

Defines additional methods that 
    requesters can use to run backup and restore operations.

To obtain an instance of the <b>IVssBackupComponentsEx2</b> 
   interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> interface, and pass 
   the <b>IID_IVssBackupComponentsEx2</b> constant as the interface identifier (IID) parameter.

## -inheritance

The <b>IVssBackupComponentsEx2</b> interface inherits from <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a> and <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>. <b>IVssBackupComponentsEx2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a>
