---
UID: NN:dskquota.IDiskQuotaUser
title: IDiskQuotaUser (dskquota.h)
description: Represents a single user quota entry in the volume quota information file.
helpviewer_keywords: ["IDiskQuotaUser","IDiskQuotaUser interface [Files]","IDiskQuotaUser interface [Files]","described","_win32_idiskquotauser","base.idiskquotauser","dskquota/IDiskQuotaUser","fs.idiskquotauser"]
old-location: fs\idiskquotauser.htm
tech.root: fs
ms.assetid: 27edbebc-35b4-4f6a-87cc-d8a99782f405
ms.date: 12/05/2018
ms.keywords: IDiskQuotaUser, IDiskQuotaUser interface [Files], IDiskQuotaUser interface [Files],described, _win32_idiskquotauser, base.idiskquotauser, dskquota/IDiskQuotaUser, fs.idiskquotauser
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
 - IDiskQuotaUser
 - dskquota/IDiskQuotaUser
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
 - IDiskQuotaUser
---

# IDiskQuotaUser interface


## -description

Represents a single user quota entry in the volume quota information file. Through this 
    interface, you can query and modify user-specific quota information on an NTFS file system 
    volume. This interface is instantiated by using 
    <a href="/windows/desktop/api/dskquota/nn-dskquota-ienumdiskquotausers">IEnumDiskQuotaUsers</a>, 
    <a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusersid">IDiskQuotaControl::FindUserSid</a>, 
    <a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusername">IDiskQuotaControl::FindUserName</a>, 
    <a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-addusersid">IDiskQuotaControl::AddUserSid</a>, or 
    <a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-addusername">IDiskQuotaControl::AddUserName</a>.

## -inheritance

The <b>IDiskQuotaUser</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiskQuotaUser</b> also has these types of members:

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>
