---
UID: NF:setupapi.SetupSetDirectoryIdA
title: SetupSetDirectoryIdA function
author: windows-driver-content
description: The SetupSetDirectoryId function associates a directory identifier in an INF file with a specific directory.
old-location: setup\setupsetdirectoryid.htm
old-project: SetupApi
ms.assetid: bacb7b90-a391-4f05-bedb-0c0f52fd15f9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SetupSetDirectoryId, SetupSetDirectoryId function [Setup API], SetupSetDirectoryIdA, SetupSetDirectoryIdW, _setupapi_setupsetdirectoryid, setup.setupsetdirectoryid, setupapi/SetupSetDirectoryId, setupapi/SetupSetDirectoryIdA, setupapi/SetupSetDirectoryIdW
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
req.unicode-ansi: SetupSetDirectoryIdW (Unicode) and SetupSetDirectoryIdA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupSetDirectoryId
-	SetupSetDirectoryIdA
-	SetupSetDirectoryIdW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SetupSetDirectoryIdA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupSetDirectoryId</b> function associates a directory identifier in an INF file with a specific directory.


## -parameters




### -param InfHandle [in]

A handle for a loaded INF file.


### -param Id [in]

A directory identifier (DIRID) to use for an association. This parameter can be <b>NULL</b>. This DIRID must be greater than or equal to DIRID_USER. If an association already exists for this DIRID, it is overwritten. If <i>Id</i> is <b>NULL</b>, the <i>Directory</i> parameter is ignored, and the current set of user-defined DIRIDs is deleted.


### -param Directory [in]

A pointer to  a <b>null</b>-terminated string that specifies the directory path to associate with <i>Id</i>. This parameter can be <b>NULL</b>. If <i>Directory</i> is <b>NULL</b>, any directory associated with <i>Id</i> is unassociated. No error results if <i>Id</i> is not currently associated with a directory.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is 0 (zero). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>SetupSetDirectoryId</b> can be used prior to queuing file copy operations to specify a target location that is only known at runtime.

After setting the directory identifier, this function traverses all appended INF files, and if any of them have unresolved string substitutions, the function attempts to re-apply string substitution to them based on the new DIRID mapping. Because of this, some INF values may change after calling 
<b>SetupSetDirectoryId</b>.

DIRID_ABSOLUTE_16BIT is not a valid value for <i>Id</i>, which ensures compatibility with 16-bit setup.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

