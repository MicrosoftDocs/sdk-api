---
UID: NF:cscobj.IOfflineFilesFileSysInfo.GetAttributes
title: IOfflineFilesFileSysInfo::GetAttributes
author: windows-sdk-content
description: Retrieves the Win32 attributes for an item.
old-location: of\iofflinefilesfilesysinfo_getattributes.htm
tech.root: offlinefiles
ms.assetid: 5bf8a834-cd5e-46b9-9b7d-b5cc6fb9fe10
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAttributes, GetAttributes method [Offline Files], GetAttributes method [Offline Files],IOfflineFilesFileSysInfo interface, IOfflineFilesFileSysInfo interface [Offline Files],GetAttributes method, IOfflineFilesFileSysInfo.GetAttributes, IOfflineFilesFileSysInfo::GetAttributes, cscobj/IOfflineFilesFileSysInfo::GetAttributes, of.iofflinefilesfilesysinfo_getattributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesFileSysInfo.GetAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesFileSysInfo::GetAttributes


## -description


Retrieves the Win32 attributes for an item.


## -parameters




### -param copy [in]

An <a href="https://msdn.microsoft.com/b956f186-962b-457e-9c03-ffd1a7f937ca">OFFLINEFILES_ITEM_COPY</a> enumeration value identifying which copy (local or remote) to retrieve the attributes for.

<b>Windows Vista:  </b>This value must be <b>OFFLINEFILES_ITEM_COPY_LOCAL</b>.


### -param pdwAttributes [out]

Receives the file attribute mask for the item.  One or more of <b>FILE_ATTRIBUTE_<i>XXXXXX</i></b> as defined in the Windows SDK. For more information, see the <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a> function.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/d3da183d-eb12-4411-b461-b58689ef5bff">IOfflineFilesFileSysInfo</a>
 

 

