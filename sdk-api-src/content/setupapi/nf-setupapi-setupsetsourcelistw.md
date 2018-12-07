---
UID: NF:setupapi.SetupSetSourceListW
title: SetupSetSourceListW function
author: windows-sdk-content
description: The SetupSetSourceList function allows the caller to set the list of installation sources for either the current user or the system (common to all users).
old-location: setup\setupsetsourcelist.htm
tech.root: SetupApi
ms.assetid: 6a37a56c-ae44-4a57-9307-90efcf025d1a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupSetSourceList, SetupSetSourceList function [Setup API], SetupSetSourceListA, SetupSetSourceListW, _setupapi_setupsetsourcelist, setup.setupsetsourcelist, setupapi/SetupSetSourceList, setupapi/SetupSetSourceListA, setupapi/SetupSetSourceListW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupSetSourceListW (Unicode) and SetupSetSourceListA (ANSI)
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
 - SetupSetSourceList
 - SetupSetSourceListA
 - SetupSetSourceListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupSetSourceListW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupSetSourceList</b> function allows the caller to set the list of installation sources for either the current user or the system (common to all users).


## -parameters




### -param Flags [in]

Specifies the type of list. This parameter can be a combination of the following values. 







#### SRCLIST_SYSTEM

The list is the per-system Most Recently Used (MRU) list stored in the registry. The caller must be a member of the administrators local group.



#### SRCLIST_USER

The list is the per-user MRU list stored in the registry.



#### SRCLIST_TEMPORARY

The specified list is temporary and will be the only list accessible to the current process until 
<a href="https://msdn.microsoft.com/87ef9425-5dab-442b-a487-3a4789005411">SetupCancelTemporarySourceList</a> is called or <b>SetSourceList</b> is called again.

<div class="alert"><b>Important</b>  If a temporary list is set, sources are not added to or deleted from the system or user lists, even if subsequent calls to 
<a href="https://msdn.microsoft.com/c1da3f9b-12ea-49f3-a5ca-45a63a56becd">SetupAddToSourceList</a> or 
<a href="https://msdn.microsoft.com/9e87f481-7d6a-4d8e-8f71-d104de3533f8">SetupRemoveFromSourceList</a> explicitly specify those lists.</div>
<div> </div>
<div class="alert"><b>Note</b>  One of the SRCLIST_SYSTEM, SRCLIST_USER, or SRCLIST_TEMPORARY flags must be specified.</div>
<div> </div>




#### SRCLIST_NOBROWSE

The user is not allowed to add or change sources when 
<a href="https://msdn.microsoft.com/65ccd3d1-1846-48cb-9fe6-ab5c69845e01">SetupPromptForDisk</a> is used. This flag is typically used in combination with the SRCLIST_TEMPORARY flag.


### -param SourceList [in]

Pointer to an array of strings to use as the source list, as specified by the <i>Flags</i> parameter.


### -param SourceCount [in]

Number of elements in the array pointed to by <i>SourceList</i>.


##### - Flags.SRCLIST_NOBROWSE

The user is not allowed to add or change sources when 
<a href="https://msdn.microsoft.com/65ccd3d1-1846-48cb-9fe6-ab5c69845e01">SetupPromptForDisk</a> is used. This flag is typically used in combination with the SRCLIST_TEMPORARY flag.


##### - Flags.SRCLIST_SYSTEM

The list is the per-system Most Recently Used (MRU) list stored in the registry. The caller must be a member of the administrators local group.


##### - Flags.SRCLIST_TEMPORARY

The specified list is temporary and will be the only list accessible to the current process until 
<a href="https://msdn.microsoft.com/87ef9425-5dab-442b-a487-3a4789005411">SetupCancelTemporarySourceList</a> is called or <b>SetSourceList</b> is called again.


##### - Flags.SRCLIST_USER

The list is the per-user MRU list stored in the registry.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/c1da3f9b-12ea-49f3-a5ca-45a63a56becd">SetupAddToSourceList</a>



<a href="https://msdn.microsoft.com/87ef9425-5dab-442b-a487-3a4789005411">SetupCancelTemporarySourceList</a>



<a href="https://msdn.microsoft.com/9e87f481-7d6a-4d8e-8f71-d104de3533f8">SetupRemoveFromSourceList</a>
 

 

