---
UID: NF:clfsw32.RemoveLogContainer
title: RemoveLogContainer function
author: windows-driver-content
description: Removes one container from a log that is associated with a dedicated or multiplexed log handle.
old-location: fs\removelogcontainer.htm
old-project: Clfs
ms.assetid: e6571cb0-8453-4db0-9a33-17339c4ea223
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: RemoveLogContainer, RemoveLogContainer function [Files], clfsw32/RemoveLogContainer, fs.removelogcontainer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfsw32.dll
api_name:
-	RemoveLogContainer
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# RemoveLogContainer function


## -description


Removes  one  container from a log that is associated with a dedicated or multiplexed log handle.

A client must have  administrative privileges on the log handle to  remove   a  container.   To remove multiple containers,  use the   <a href="https://msdn.microsoft.com/adc35813-7368-4d8c-ad2b-1bb0824ad019">RemoveLogContainerSet</a>  function.


## -parameters




### -param hLog [in]

A handle to the log that is obtained from <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>.


### -param pwszContainerPath [in]

A pointer to a wide character string that contains a  path for a  log container that is created by either  <a href="https://msdn.microsoft.com/5e886b96-9431-43f6-b888-e0f47c432371">AddLogContainer</a> or <a href="https://msdn.microsoft.com/b3dec3bd-3e39-42fa-8f73-71784b3d5be2">AddLogContainerSet</a>.


### -param fForce [in]

The deletion flag  that determines when and how a container is deleted.

If <i>fForce</i> is <b>TRUE</b>, and the container is part of the active log region, the container is not deleted and an error <b>ERROR_LOG_CANT_DELETE</b> is returned.

If <b>FALSE</b>, the container is deleted when the container is no longer a part of the active log region.


### -param pReserved [in, out, optional]

This parameter is reserved and should be  set to <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

 The following list identifies the possible error codes:




## -remarks



  By default, container deletion is lazy, which means that a container is deleted  only if it is not part of an active log.  If the container is part of the active log, it is marked for deletion. However,  deletion does not occur until the  end  of the log exceeds the last sector of the container, or the container has a logical identifier that is greater than the logical identifier of the head of the active log.  The log size reflects the container deletion only when the container is deleted physically.

A log client can request a forced deletion on a container by setting the deletion flag to <b>TRUE</b>. This has the same effect  as deleting a container  that  is  not part of the active log.  However, if the container is part of the active log, the call fails without marking the container for deletion.




## -see-also




<a href="https://msdn.microsoft.com/5e886b96-9431-43f6-b888-e0f47c432371">AddLogContainer</a>



<a href="https://msdn.microsoft.com/b3dec3bd-3e39-42fa-8f73-71784b3d5be2">AddLogContainerSet</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/adc35813-7368-4d8c-ad2b-1bb0824ad019">RemoveLogContainerSet</a>
 

 

