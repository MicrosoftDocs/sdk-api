---
UID: NF:userenv.DestroyEnvironmentBlock
title: DestroyEnvironmentBlock function (userenv.h)
author: windows-sdk-content
description: Frees environment variables created by the CreateEnvironmentBlock function.
old-location: shell\DestroyEnvironmentBlock.htm
tech.root: shell
ms.assetid: 8d03e102-3f8a-4aa7-b175-0a6781eedea7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DestroyEnvironmentBlock, DestroyEnvironmentBlock function [Windows Shell], _shell_DestroyEnvironmentBlock, shell.DestroyEnvironmentBlock, userenv/DestroyEnvironmentBlock
ms.topic: function
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - DestroyEnvironmentBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DestroyEnvironmentBlock function


## -description


Frees environment variables created by the <a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-createenvironmentblock">CreateEnvironmentBlock</a> function.


## -parameters




### -param lpEnvironment [in]

Type: <b>LPVOID</b>

Pointer to the environment block created by 
<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-createenvironmentblock">CreateEnvironmentBlock</a>. The environment block is an array of null-terminated Unicode strings. The list ends with two nulls (\0\0).


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-createenvironmentblock">CreateEnvironmentBlock</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>
 

 

