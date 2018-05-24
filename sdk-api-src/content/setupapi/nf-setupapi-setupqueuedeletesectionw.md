---
UID: NF:setupapi.SetupQueueDeleteSectionW
title: SetupQueueDeleteSectionW function
author: windows-driver-content
description: The SetupQueueDeleteSection function queues all the files in a section of an INF file for deletion. The section must be in the correct Delete Files format and the INF file must contain a DestinationDirs section.
old-location: setup\setupqueuedeletesection.htm
old-project: SetupApi
ms.assetid: 3e76e345-1d6c-4eb5-a743-b71d5ccc52e5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SetupQueueDeleteSection, SetupQueueDeleteSection function [Setup API], SetupQueueDeleteSectionA, SetupQueueDeleteSectionW, _setupapi_setupqueuedeletesection, setup.setupqueuedeletesection, setupapi/SetupQueueDeleteSection, setupapi/SetupQueueDeleteSectionA, setupapi/SetupQueueDeleteSectionW
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
req.unicode-ansi: SetupQueueDeleteSectionW (Unicode) and SetupQueueDeleteSectionA (ANSI)
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
-	SetupQueueDeleteSection
-	SetupQueueDeleteSectionA
-	SetupQueueDeleteSectionW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupQueueDeleteSectionW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupQueueDeleteSection</b> function queues all the files in a section of an INF file for deletion. The section must be in the correct <b>Delete Files</b> format and the INF file must contain a <b>DestinationDirs</b> section.


## -parameters




### -param QueueHandle [in]

Handle to a setup file queue, as returned by 
<a href="https://msdn.microsoft.com/36950f18-80ae-46b7-9f9f-bd5307d72a3b">SetupOpenFileQueue</a>.


### -param InfHandle [in]

Handle to an open INF file that contains the <b>DestinationDirs</b> section. If <i>ListInfHandle</i> is not specified, <i>InfHandle</i> contains the section name. 


### -param ListInfHandle [in]

Optional  handle to an open INF file that contains the section to queue for deletion. If <i>ListInfHandle</i> is not specified, <i>InfHandle</i> is assumed to contain the section name.


### -param Section [in]

Pointer to a  null-terminated string that specifies the name of the section to be queued for deletion.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function requires a Windows INF file. Some older INF file  formats may not be supported. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/f61fd00e-e60f-4722-9da7-1ed4d8491004">SetupQueueCopySection</a>



<a href="https://msdn.microsoft.com/21cdaf05-c4fb-4130-baa5-31baf5391ece">SetupQueueDelete</a>



<a href="https://msdn.microsoft.com/8ac93cfa-cfe4-4747-813d-512963d0d87c">SetupQueueRenameSection</a>
 

 

