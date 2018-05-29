---
UID: NF:wuapi.IUpdate.get_RecommendedMemory
title: IUpdate::get_RecommendedMemory
author: windows-sdk-content
description: Gets the recommended physical memory size that should be available in your computer before you install the update. The physical memory size is specified in megabytes (MB).
old-location: wua\iupdate_recommendedmemory.htm
old-project: Wua_Sdk
ms.assetid: 68a8341b-ba0a-4694-89c3-34fefb950bf7
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IUpdate interface [Windows Update Agent],RecommendedMemory property, IUpdate.RecommendedMemory, IUpdate.get_RecommendedMemory, IUpdate::RecommendedMemory, IUpdate::get_RecommendedMemory, RecommendedMemory property [Windows Update Agent], RecommendedMemory property [Windows Update Agent],IUpdate interface, get_RecommendedMemory, wua.iupdate_recommendedmemory, wuapi/IUpdate::RecommendedMemory, wuapi/IUpdate::get_RecommendedMemory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdate.RecommendedMemory
-	IUpdate.get_RecommendedMemory
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdate::get_RecommendedMemory


## -description


Gets the recommended physical memory size that should be available in your  computer before you install the update. The physical memory size is specified in megabytes (MB).

This property is read-only.


## -parameters


## -remarks



The following properties of the <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> interface return 0 (zero) when the information is not available:

<ul>
<li>
<a href="https://msdn.microsoft.com/21003be2-c14e-48d4-a51f-ed75b1b47284">RecommendedCpuSpeed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/958d3de3-b2e0-47e0-9a71-b12ff6669242">RecommendedHardDiskSpace</a>
</li>
<li><b>RecommendedMemory</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 

