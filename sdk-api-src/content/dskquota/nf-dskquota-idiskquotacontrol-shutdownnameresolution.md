---
UID: NF:dskquota.IDiskQuotaControl.ShutdownNameResolution
title: IDiskQuotaControl::ShutdownNameResolution
author: windows-sdk-content
description: Translates user security identifiers (SID) to user names.
old-location: fs\idiskquotacontrol_shutdownnameresolution.htm
old-project: fileio
ms.assetid: 53a2dd49-46e8-4e84-bbc2-102a57f36abc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDiskQuotaControl interface [Files],ShutdownNameResolution method, IDiskQuotaControl.ShutdownNameResolution, IDiskQuotaControl::ShutdownNameResolution, ShutdownNameResolution, ShutdownNameResolution method [Files], ShutdownNameResolution method [Files],IDiskQuotaControl interface, _win32_idiskquotacontrol_shutdownnameresolution, base.idiskquotacontrol_shutdownnameresolution, dskquota/IDiskQuotaControl::ShutdownNameResolution, fs.idiskquotacontrol_shutdownnameresolution
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dskquota.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaControl.ShutdownNameResolution
product: Windows
targetos: Windows
req.lib: 
req.dll: Dskquota.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDiskQuotaControl::ShutdownNameResolution


## -description


The SID-to-name resolver translates user security identifiers (SID) to user names. It runs as a background thread. When a quota control object is destroyed, this thread automatically terminates. The final call to the <a href="_com_iunknown_release">IUnknown::Release</a> method terminates the thread. This is normally all that is required. If you finish with the quota control object, but it is not ready to be destroyed (there are other open reference counts), call this method to terminate the background thread before the object is destroyed.


## -parameters






## -returns



This method returns <b>S_OK</b>.




## -remarks



Asynchronous name resolution will also cease after the thread terminates. A subsequent call to the following methods can re-create the SID-to-name resolver thread:

<ul>
<li>
<a href="https://msdn.microsoft.com/306120e8-642a-439d-839c-944cb7fd7ee2">IDiskQuotaControl::AddUserName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a82b36a9-7270-4b4a-b850-67916864c052">IDiskQuotaControl::AddUserSid</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a29e1955-80e2-442d-9565-c885006be565">IDiskQuotaControl::CreateEnumUsers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dae4e2d4-0293-4ee4-9687-9fed4b3a3600">IDiskQuotaControl::FindUserName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a6ce8eb3-cfa3-43b4-80ee-6dbef41f99ac">IDiskQuotaControl::FindUserSid</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/fc9add5a-c9ef-462d-8125-128d48018717">IDiskQuotaControl</a>
 

 

