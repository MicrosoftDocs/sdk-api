---
UID: NF:dskquota.IDiskQuotaControl.ShutdownNameResolution
title: IDiskQuotaControl::ShutdownNameResolution (dskquota.h)
description: Translates user security identifiers (SID) to user names.
helpviewer_keywords: ["IDiskQuotaControl interface [Files]","ShutdownNameResolution method","IDiskQuotaControl.ShutdownNameResolution","IDiskQuotaControl::ShutdownNameResolution","ShutdownNameResolution","ShutdownNameResolution method [Files]","ShutdownNameResolution method [Files]","IDiskQuotaControl interface","_win32_idiskquotacontrol_shutdownnameresolution","base.idiskquotacontrol_shutdownnameresolution","dskquota/IDiskQuotaControl::ShutdownNameResolution","fs.idiskquotacontrol_shutdownnameresolution"]
old-location: fs\idiskquotacontrol_shutdownnameresolution.htm
tech.root: fs
ms.assetid: 53a2dd49-46e8-4e84-bbc2-102a57f36abc
ms.date: 12/05/2018
ms.keywords: IDiskQuotaControl interface [Files],ShutdownNameResolution method, IDiskQuotaControl.ShutdownNameResolution, IDiskQuotaControl::ShutdownNameResolution, ShutdownNameResolution, ShutdownNameResolution method [Files], ShutdownNameResolution method [Files],IDiskQuotaControl interface, _win32_idiskquotacontrol_shutdownnameresolution, base.idiskquotacontrol_shutdownnameresolution, dskquota/IDiskQuotaControl::ShutdownNameResolution, fs.idiskquotacontrol_shutdownnameresolution
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
 - IDiskQuotaControl::ShutdownNameResolution
 - dskquota/IDiskQuotaControl::ShutdownNameResolution
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
 - IDiskQuotaControl.ShutdownNameResolution
---

# IDiskQuotaControl::ShutdownNameResolution


## -description

The SID-to-name resolver translates user security identifiers (SID) to user names. It runs as a background thread. When a quota control object is destroyed, this thread automatically terminates. The final call to the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method terminates the thread. This is normally all that is required. If you finish with the quota control object, but it is not ready to be destroyed (there are other open reference counts), call this method to terminate the background thread before the object is destroyed.



## -returns

This method returns <b>S_OK</b>.

## -remarks

Asynchronous name resolution will also cease after the thread terminates. A subsequent call to the following methods can re-create the SID-to-name resolver thread:

<ul>
<li>
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-addusername">IDiskQuotaControl::AddUserName</a>
</li>
<li>
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-addusersid">IDiskQuotaControl::AddUserSid</a>
</li>
<li>
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-createenumusers">IDiskQuotaControl::CreateEnumUsers</a>
</li>
<li>
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusername">IDiskQuotaControl::FindUserName</a>
</li>
<li>
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-findusersid">IDiskQuotaControl::FindUserSid</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>



<a href="/windows/desktop/api/dskquota/nn-dskquota-idiskquotacontrol">IDiskQuotaControl</a>
