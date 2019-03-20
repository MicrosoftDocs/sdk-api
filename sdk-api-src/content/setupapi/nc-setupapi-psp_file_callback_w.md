---
UID: NC:setupapi.PSP_FILE_CALLBACK_W
title: PSP_FILE_CALLBACK_W (setupapi.h)
author: windows-sdk-content
description: The FileCallback callback function is used by a few setup functions.
old-location: setup\psp_file_callback.htm
tech.root: SetupApi
ms.assetid: 41eaa57a-e116-443c-93ee-397456a5c466
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FileCallback, PSP_FILE_CALLBACK, PSP_FILE_CALLBACK callback, PSP_FILE_CALLBACK callback function [Setup API], PSP_FILE_CALLBACK_A, PSP_FILE_CALLBACK_W, _setupapi_psp_file_callback, setup.psp_file_callback, setupapi/PSP_FILE_CALLBACK
ms.topic: callback
req.header: setupapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - setupapi.h
api_name:
 - PSP_FILE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSP_FILE_CALLBACK_W callback function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<i>FileCallback</i> callback function is used by a few setup functions. The <b>PSP_FILE_CALLBACK</b> type defines a pointer to this callback function. <i>FileCallback</i> is a placeholder for the application-defined function name.

For more information, see 
<a href="https://msdn.microsoft.com/93434558-ae83-4ea2-9324-659e5873a8c3">Notifications</a>, 
<a href="https://msdn.microsoft.com/68781565-71a2-43bf-ad01-7c1cdc514f7b">Creating a Custom Queue Callback Routine</a>, and 
<a href="https://msdn.microsoft.com/45a2690e-1db6-4a09-a141-9e68ebc2a6d8">Creating a Cabinet Callback Routine</a>.


## -parameters




### -param Context

The context information about the queue notification  that is returned to the callback function.


### -param Notification

The event that triggers the call to the callback function.


### -param Param1

The additional notification information. The value is dependent on the notification that is being returned.


### -param Param2

The additional notification information. The value is dependent on the notification that is being returned.


## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/c532f435-7393-49f0-975c-4c0ecca64407">SetupCommitFileQueue</a>



<a href="https://msdn.microsoft.com/04db1553-1c9a-414e-a2b8-b087dd44ef55">SetupInstallFile</a>



<a href="https://msdn.microsoft.com/56013a33-341f-4b6b-a428-ec5aa0981835">SetupInstallFileEx</a>



<a href="https://msdn.microsoft.com/bd1ee91a-b58b-4f08-9181-42fbe9d763f9">SetupInstallFromInfSection</a>



<a href="https://msdn.microsoft.com/2fa2d140-fa8e-41a8-9800-d10e5559fab4">SetupIterateCabinet</a>
 

 

