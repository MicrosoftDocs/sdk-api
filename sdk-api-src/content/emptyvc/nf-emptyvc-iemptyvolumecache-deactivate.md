---
UID: NF:emptyvc.IEmptyVolumeCache.Deactivate
title: IEmptyVolumeCache::Deactivate method
author: windows-driver-content
description: Notifies the handler that the disk cleanup manager is shutting down.
old-location: lwef\iemptyvolumecache_deactivate.htm
old-project: lwef
ms.assetid: fb374e09-92f5-4efb-8e93-0ddc2975c2c1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Deactivate method [Legacy Windows Environment Features], Deactivate method [Legacy Windows Environment Features], IEmptyVolumeCache interface, Deactivate,IEmptyVolumeCache.Deactivate, EVCF_REMOVEFROMLIST, IEmptyVolumeCache, IEmptyVolumeCache interface [Legacy Windows Environment Features], Deactivate method, IEmptyVolumeCache::Deactivate, _win32_IEmptyVolumeCache_Deactivate, emptyvc/IEmptyVolumeCache::Deactivate, lwef.iemptyvolumecache_deactivate, shell.iemptyvolumecache_deactivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: emptyvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.typenames: MAPPING_SERVICE_INFO, *PMAPPING_SERVICE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IEmptyVolumeCache.Deactivate
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEmptyVolumeCache::Deactivate method


## -description


Notifies the handler that the disk cleanup manager is shutting down. 


## -parameters




### -param pdwFlags [out]

Type: <b>DWORD*</b>

A flag that can be set to return information to the disk cleanup manager. It can have the following value. 



#### EVCF_REMOVEFROMLIST

If this flag is set, the disk cleanup manager will delete the handler's registry subkey. 


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
This value should always be returned.

</td>
</tr>
</table>
 




## -remarks



If the <b>EVCF_REMOVEFROMLIST</b> flag is set, the handler will not be run again unless the registry entries are reestablished. This flag is typically used for a handler that will only run once.



