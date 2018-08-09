---
UID: NF:setupapi.SetupBackupErrorW
title: SetupBackupErrorW function
author: windows-sdk-content
description: The SetupBackupError function generates a dialog box that informs the user of a backup error.
old-location: setup\setupbackuperror.htm
old-project: SetupApi
ms.assetid: 4c2a8a63-29e7-4750-9239-6693754dff58
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: SetupBackupError, SetupBackupError function [Setup API], SetupBackupErrorA, SetupBackupErrorW, _setupapi_setupbackuperror, setup.setupbackuperror, setupapi/SetupBackupError, setupapi/SetupBackupErrorA, setupapi/SetupBackupErrorW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupBackupErrorW (Unicode) and SetupBackupErrorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupBackupError
 - SetupBackupErrorA
 - SetupBackupErrorW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupBackupErrorW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupBackupError</b> function generates a dialog box that informs the user of a backup error.


## -parameters




### -param hwndParent [in]

Handle to the parent window for this dialog box.


### -param DialogTitle [in]

Optional pointer to a <b>null</b>-terminated string specifying the error dialog box title. If this parameter is <b>NULL</b>, the default title of "Backup Error" (localized) is used.


### -param SourceFile [in]

Pointer to a <b>null</b>-terminated string specifying the full path of the source file that is being backed up.


### -param TargetFile [in]

Optional pointer to a <b>null</b>-terminated string specifying the full path of the backup name of the file. This parameter can be <b>NULL</b>.



### -param Win32ErrorCode [out]

If an error occurs, this member is the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. If no error has occurred, it is  NO_ERROR.


### -param Style [in]

Flags that control display formatting and behavior of the dialog box. This parameter can be one of the following flags. 







#### IDF_NOBEEP

Prevent the dialog box from beeping to get the user's attention when it first appears.



#### IDF_NOFOREGROUND

Prevent the dialog box from becoming the foreground window.


##### - Style.IDF_NOBEEP

Prevent the dialog box from beeping to get the user's attention when it first appears.


##### - Style.IDF_NOFOREGROUND

Prevent the dialog box from becoming the foreground window.


## -returns



This function returns one of the following values.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/bda8ffef-f1a7-474c-9ec6-f76c2f006d51">SetupCopyError</a>



<a href="https://msdn.microsoft.com/200e1926-7ebd-4373-803d-1c054db5df8d">SetupDeleteError</a>



<a href="https://msdn.microsoft.com/65ccd3d1-1846-48cb-9fe6-ab5c69845e01">SetupPromptForDisk</a>



<a href="https://msdn.microsoft.com/43371fa0-d7b4-42e0-a94d-d307a7210618">SetupRenameError</a>
 

 

