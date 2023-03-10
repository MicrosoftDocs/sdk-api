---
UID: NN:dskquota.IDiskQuotaControl
title: IDiskQuotaControl (dskquota.h)
description: Controls the disk quota facilities of a single NTFS file system volume.
helpviewer_keywords: ["IDiskQuotaControl","IDiskQuotaControl interface [Files]","IDiskQuotaControl interface [Files]","described","_win32_idiskquotacontrol","base.idiskquotacontrol","dskquota/IDiskQuotaControl","fs.idiskquotacontrol"]
old-location: fs\idiskquotacontrol.htm
tech.root: fs
ms.assetid: fc9add5a-c9ef-462d-8125-128d48018717
ms.date: 12/05/2018
ms.keywords: IDiskQuotaControl, IDiskQuotaControl interface [Files], IDiskQuotaControl interface [Files],described, _win32_idiskquotacontrol, base.idiskquotacontrol, dskquota/IDiskQuotaControl, fs.idiskquotacontrol
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
 - IDiskQuotaControl
 - dskquota/IDiskQuotaControl
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
 - IDiskQuotaControl
---

# IDiskQuotaControl interface


## -description

Controls the disk quota facilities of a single NTFS file system volume. The client can query and set volume-specific quota attributes through 
<b>IDiskQuotaControl</b>. The client can also enumerate all per-user quota entries on the volume. A client instantiates this interface by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function using the class identifier CLSID_DiskQuotaControl.

## -inheritance

The <b>IDiskQuotaControl</b> interface inherits from the <a href="/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> interface. <b>IDiskQuotaControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>
