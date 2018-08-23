---
UID: NF:dskquota.IDiskQuotaUser.GetID
title: IDiskQuotaUser::GetID
author: windows-sdk-content
description: Retrieves a unique identifier (ID) number for the DiskQuotaUser object.
old-location: fs\idiskquotauser_getid.htm
old-project: fileio
ms.assetid: 04f84fd1-9ce4-4daa-91b3-24508f326f84
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetID, GetID method [Files], GetID method [Files],IDiskQuotaUser interface, IDiskQuotaUser interface [Files],GetID method, IDiskQuotaUser.GetID, IDiskQuotaUser::GetID, _win32_idiskquotauser_getid, base.idiskquotauser_getid, dskquota/IDiskQuotaUser::GetID, fs.idiskquotauser_getid
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
 - IDiskQuotaUser.GetID
product: Windows
targetos: Windows
req.lib: 
req.dll: Dskquota.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDiskQuotaUser::GetID


## -description


Retrieves a unique identifier (ID) number for the <a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">DiskQuotaUser</a> object. This ID is unique only within the process. It can be used to identify a user object in a set of user objects if the programming language you are using does not support pointers.


## -parameters




### -param pulID [out]

The name strings associated with the disk quota user.


## -returns



This method returns <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/27edbebc-35b4-4f6a-87cc-d8a99782f405">IDiskQuotaUser</a>
 

 

