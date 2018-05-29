---
UID: NF:xaudio2.IXAudio2.CommitChanges
title: IXAudio2::CommitChanges
author: windows-sdk-content
description: Atomically applies a set of operations that are tagged with a given identifier.
old-location: xaudio2\ixaudio2_interface_commitchanges.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.CommitChanges(UINT32)
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: CommitChanges, CommitChanges method [XAudio2 Audio Mixing APIs], CommitChanges method [XAudio2 Audio Mixing APIs],IXAudio2 interface, IXAudio2 interface [XAudio2 Audio Mixing APIs],CommitChanges method, IXAudio2.CommitChanges, IXAudio2::CommitChanges, xaudio2.ixaudio2_interface_commitchanges, xaudio2/IXAudio2::CommitChanges
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xaudio2.h
api_name:
-	IXAudio2.CommitChanges
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2::CommitChanges


## -description


Atomically applies a set of operations that are tagged with a given identifier.


## -parameters




### -param OperationSet [in]

Identifier of the set of operations to be applied. To commit all pending operations, pass <b>XAUDIO2_COMMIT_ALL</b>. 


## -returns



Returns S_OK if successful; returns an error code otherwise. See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.




## -remarks



<b>CommitChanges</b> does nothing if no operations are tagged with the given identifier.



See the <a href="https://msdn.microsoft.com/5bfd747d-af65-f619-e549-be8130748261">XAudio2 Operation Sets</a> overview about working with <b>CommitChanges</b> and XAudio2 interface methods that may be deferred.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/A49469C6-2C29-407C-8C57-65E3FC9463F1">IXAudio2</a>
 

 

