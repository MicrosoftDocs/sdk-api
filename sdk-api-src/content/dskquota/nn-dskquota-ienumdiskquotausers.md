---
UID: NN:dskquota.IEnumDiskQuotaUsers
title: IEnumDiskQuotaUsers (dskquota.h)
description: Enumerates user quota entries on the volume.
helpviewer_keywords: ["IEnumDiskQuotaUsers","IEnumDiskQuotaUsers interface [Files]","IEnumDiskQuotaUsers interface [Files]","described","_win32_ienumdiskquotausers","base.ienumdiskquotausers","dskquota/IEnumDiskQuotaUsers","fs.ienumdiskquotausers"]
old-location: fs\ienumdiskquotausers.htm
tech.root: fs
ms.assetid: f5916b17-66ed-46d4-87f1-5ee2ef57c1a1
ms.date: 12/05/2018
ms.keywords: IEnumDiskQuotaUsers, IEnumDiskQuotaUsers interface [Files], IEnumDiskQuotaUsers interface [Files],described, _win32_ienumdiskquotausers, base.ienumdiskquotausers, dskquota/IEnumDiskQuotaUsers, fs.ienumdiskquotausers
req.header: dskquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Dskquota.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumDiskQuotaUsers
 - dskquota/IEnumDiskQuotaUsers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IEnumDiskQuotaUsers
---

# IEnumDiskQuotaUsers interface


## -description

Enumerates user quota entries on the volume. This interface is instantiated by using the 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-createenumusers">IDiskQuotaControl::CreateEnumUsers</a> method.

## -inheritance

The <b>IEnumDiskQuotaUsers</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumDiskQuotaUsers</b> also has these types of members:

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>
