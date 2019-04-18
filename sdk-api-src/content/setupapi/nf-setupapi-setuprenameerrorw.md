---
UID: NF:setupapi.SetupRenameErrorW
title: SetupRenameErrorW function (setupapi.h)
author: windows-sdk-content
description: The RenameError function generates a dialog box that informs the user of a file renaming error.
old-location: setup\setuprenameerror.htm
tech.root: SetupApi
ms.assetid: 43371fa0-d7b4-42e0-a94d-d307a7210618
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupRenameError, SetupRenameError function [Setup API], SetupRenameErrorA, SetupRenameErrorW, _setupapi_setuprenameerror, setup.setuprenameerror, setupapi/SetupRenameError, setupapi/SetupRenameErrorA, setupapi/SetupRenameErrorW
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupRenameErrorW (Unicode) and SetupRenameErrorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupRenameError
 - SetupRenameErrorA
 - SetupRenameErrorW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupRenameErrorW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>RenameError</b> function generates a dialog box that informs the user of a file renaming error.


## -parameters




### -param hwndParent [in]

Handle to the parent window for this dialog box.


### -param DialogTitle [in]

Pointer to a <b>null</b>-terminated string that specifies the error dialog box title. This parameter may be <b>NULL</b>. If this parameter is <b>NULL</b>, the default title of "Rename Error" (localized) is used.


### -param SourceFile [in]

Pointer to a <b>null</b>-terminated string that specifies the full path of the source file on which the operation failed.


### -param TargetFile [in]

Pointer to a <b>null</b>-terminated string that specifies the full path of the target file on which the operation failed.


### -param Win32ErrorCode [in]

The <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> encountered during the file operation. 


### -param Style [in]

Specifies display formatting and behavior of the dialog box. This parameter can be one of the following flags. 







#### IDF_NOBEEP

Prevent the dialog box from beeping when it first appears.



#### IDF_NOFOREGROUND

Prevent the dialog box from becoming the foreground window.


##### - Style.IDF_NOBEEP

Prevent the dialog box from beeping when it first appears.


##### - Style.IDF_NOFOREGROUND

Prevent the dialog box from becoming the foreground window.


## -returns



This function returns one of the following values.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/bda8ffef-f1a7-474c-9ec6-f76c2f006d51">SetupCopyError</a>



<a href="https://msdn.microsoft.com/200e1926-7ebd-4373-803d-1c054db5df8d">SetupDeleteError</a>



<a href="https://msdn.microsoft.com/65ccd3d1-1846-48cb-9fe6-ab5c69845e01">SetupPromptForDisk</a>
 

 

