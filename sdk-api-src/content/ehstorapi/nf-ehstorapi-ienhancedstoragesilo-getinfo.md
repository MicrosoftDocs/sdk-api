---
UID: NF:ehstorapi.IEnhancedStorageSilo.GetInfo
title: IEnhancedStorageSilo::GetInfo
author: windows-sdk-content
description: Returns the descriptive information associated with the silo object.
old-location: enstor\ienhancedstoragesilo_getinfo.htm
old-project: enstor
ms.assetid: c3d84462-fb2c-4ad7-b539-1d6c775812dd
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetInfo, GetInfo method [Enhanced Storage], GetInfo method [Enhanced Storage],IEnhancedStorageSilo interface, IEnhancedStorageSilo interface [Enhanced Storage],GetInfo method, IEnhancedStorageSilo.GetInfo, IEnhancedStorageSilo::GetInfo, ehstorapi/IEnhancedStorageSilo::GetInfo, enstor.ienhancedstoragesilo_getinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TimedLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EhStorAPI.h
api_name:
-	IEnhancedStorageSilo.GetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnhancedStorageSilo::GetInfo


## -description


Returns the descriptive information associated with the silo object.


## -parameters




### -param pSiloInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/8bfe7c31-61e0-420b-8b6b-6b014cd5e243">SILO_INFO</a> object containing descriptive information associated with the silo.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
Silo information was retrieved successfully. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/041e66d2-f772-407d-85f7-71f226c7ec4b">IEnhancedStorageSilo</a>
 

 

