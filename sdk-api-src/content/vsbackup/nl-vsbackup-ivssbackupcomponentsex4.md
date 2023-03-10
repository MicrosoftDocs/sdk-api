---
UID: NL:vsbackup.IVssBackupComponentsEx4
title: IVssBackupComponentsEx4 (vsbackup.h)
description: Defines additional methods to support the processing of UNC file share paths in a requester.
helpviewer_keywords: ["IVssBackupComponentsEx4","IVssBackupComponentsEx4 interface","IVssBackupComponentsEx4 interface","described","base.ivssbackupcomponentsex4","vsbackup/IVssBackupComponentsEx4"]
old-location: base\ivssbackupcomponentsex4.htm
tech.root: base
ms.assetid: 3D72F6FC-4EAA-49F9-9652-AC314FFAB504
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx4, IVssBackupComponentsEx4 interface, IVssBackupComponentsEx4 interface,described, base.ivssbackupcomponentsex4, vsbackup/IVssBackupComponentsEx4
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IVssBackupComponentsEx4
 - vsbackup/IVssBackupComponentsEx4
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
 - IVssBackupComponentsEx4
---

# IVssBackupComponentsEx4 class


## -description

Defines additional methods to support the processing of UNC file share paths in a requester.

To obtain an instance of the <b>IVssBackupComponentsEx4</b> 
   interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> interface, and pass 
   the <b>IID_IVssBackupComponentsEx4</b> constant as the interface identifier (IID) parameter.

## -inheritance

The <b>IVssBackupComponentsEx4</b> interface inherits from <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex3">IVssBackupComponentsEx3</a>, <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex2">IVssBackupComponentsEx2</a>, <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a>, and <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>. <b>IVssBackupComponentsEx4</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex2">IVssBackupComponentsEx2</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex3">IVssBackupComponentsEx3</a>
