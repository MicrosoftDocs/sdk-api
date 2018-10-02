---
UID: NF:cscobj.IEnumOfflineFilesSettings.Next
title: IEnumOfflineFilesSettings::Next
author: windows-sdk-content
description: Retrieves the next item in the enumeration and advances the enumerator.
old-location: of\ienumofflinefilessettings_next.htm
tech.root: OfflineFiles
ms.assetid: 00230021-6069-4e0b-a3d6-95651aa6e44a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IEnumOfflineFilesSettings interface [Offline Files],Next method, IEnumOfflineFilesSettings.Next, IEnumOfflineFilesSettings::Next, Next, Next method [Offline Files], Next method [Offline Files],IEnumOfflineFilesSettings interface, cscobj/IEnumOfflineFilesSettings::Next, of.ienumofflinefilessettings_next
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
 - IEnumOfflineFilesSettings.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumOfflineFilesSettings::Next


## -description


Retrieves the next item in the enumeration and advances the enumerator.


## -parameters




### -param celt [in]

Number of elements requested.


### -param rgelt [out]

Array of elements returned.


### -param pceltFetched [out]

Number of elements returned.


## -returns



Returns <b>S_OK</b> if the number of elements returned is <i>celt</i>; S_FALSE if a number less than <i>celt</i> is returned; or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530481(v=VS.85).aspx">IEnumOfflineFilesSettings</a>
 

 

