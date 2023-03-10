---
UID: NL:vsbackup.IVssBackupComponentsEx3
title: IVssBackupComponentsEx3 (vsbackup.h)
description: Defines additional methods that requesters can use to perform LUN resynchronization and return extended writer status information.
helpviewer_keywords: ["IVssBackupComponentsEx3","IVssBackupComponentsEx3 interface","IVssBackupComponentsEx3 interface","described","base.ivssbackupcomponentsex3","vsbackup/IVssBackupComponentsEx3"]
old-location: base\ivssbackupcomponentsex3.htm
tech.root: base
ms.assetid: 56c8e7c2-2d94-4674-bd20-bf036991474f
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx3, IVssBackupComponentsEx3 interface, IVssBackupComponentsEx3 interface,described, base.ivssbackupcomponentsex3, vsbackup/IVssBackupComponentsEx3
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponentsEx3
 - vsbackup/IVssBackupComponentsEx3
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
 - IVssBackupComponentsEx3
---

# IVssBackupComponentsEx3 class


## -description

Defines additional methods that 
    requesters can use to perform LUN resynchronization and return extended writer status information.

To obtain an instance of the <b>IVssBackupComponentsEx3</b> 
   interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> interface, and pass 
   the <b>IID_IVssBackupComponentsEx3</b> constant as the interface identifier (IID) parameter.

## -inheritance

The <b>IVssBackupComponentsEx3</b> interface inherits from <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex2">IVssBackupComponentsEx2</a>, <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a>, and <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>. <b>IVssBackupComponentsEx3</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex2">IVssBackupComponentsEx2</a>
