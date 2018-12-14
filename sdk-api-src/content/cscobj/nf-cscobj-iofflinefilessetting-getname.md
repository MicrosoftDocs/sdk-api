---
UID: NF:cscobj.IOfflineFilesSetting.GetName
title: IOfflineFilesSetting::GetName
author: windows-sdk-content
description: Retrieves a name associated with a particular Offline Files setting.
old-location: of\iofflinefilessetting_getname.htm
tech.root: offlinefiles
ms.assetid: 2e4591b5-c8a9-4645-8001-8ac09c706ee2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetName, GetName method [Offline Files], GetName method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],GetName method, IOfflineFilesSetting.GetName, IOfflineFilesSetting::GetName, cscobj/IOfflineFilesSetting::GetName, of.iofflinefilessetting_getname
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
 - IOfflineFilesSetting.GetName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSetting::GetName


## -description


Retrieves a name associated with a particular Offline Files setting.


## -parameters




### -param ppszName [out]

Address of pointer variable that receives the address of a string containing the name of the Offline Files setting.  Upon successful return, the caller must free this memory block by using the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a>
 

 

