---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _OFNOTIFYA structure


## -description


Contains information about a <a href="_win32_WM_NOTIFY">WM_NOTIFY</a> message sent to an <a href="https://msdn.microsoft.com/3d3a7878-1ccc-4832-9351-8f9cf6c7a601">OFNHookProc</a> hook procedure for an <b>Open</b> or <b>Save As</b> dialog box. The <i>lParam</i> parameter of the <b>WM_NOTIFY</b> message is a pointer to an <b>OFNOTIFY</b> structure. 


## -struct-fields




### -field hdr

Type: <b><a href="controls._win32_NMHDR_str">NMHDR</a></b>

The <b>code</b> member of this structure can be one of the following notification messages that identify the message being sent: <a href="https://msdn.microsoft.com/7f3de96f-68d8-4f40-b74f-304835f9def2">CDN_FILEOK</a>, <a href="https://msdn.microsoft.com/864ab80d-cd99-4dd6-8aff-49beed246e53">CDN_FOLDERCHANGE</a>, <a href="https://msdn.microsoft.com/18ee86b2-3446-4de4-a47a-2e44e677f4f7">CDN_HELP</a>, <a href="https://msdn.microsoft.com/337fccac-5444-442d-92f0-862c5302fa21">CDN_INITDONE</a>, <a href="https://msdn.microsoft.com/e622babf-7024-45c5-a8db-f80896f69140">CDN_SELCHANGE</a>, <a href="https://msdn.microsoft.com/a62ca550-0997-4379-aaaf-a5bc9414bd69">CDN_SHAREVIOLATION</a>, <a href="https://msdn.microsoft.com/fb8324db-e435-4ef2-aac5-506a6b7adb2c">CDN_TYPECHANGE</a>. 


### -field lpOFN

Type: <b>LPOPENFILENAME</b>

A pointer to the <a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a> structure that was specified when the <b>Open</b> or <b>Save As</b> dialog box was created. For some of the notification messages, this structure contains additional information about the event that caused the notification. 


### -field pszFile

Type: <b>LPTSTR</b>

The file name for which a network sharing violation has occurred. This member is valid only with the <a href="https://msdn.microsoft.com/a62ca550-0997-4379-aaaf-a5bc9414bd69">CDN_SHAREVIOLATION</a> notification message. 


## -remarks



Not all of the <b>Open</b> and <b>Save As</b> notification messages use the <b>OFNOTIFY</b> structure. The <a href="https://msdn.microsoft.com/0972a78d-e058-4bac-85bd-fbd4c3885552">CDN_INCLUDEITEM</a> notification message uses the <a href="https://msdn.microsoft.com/0efe3e60-b300-49c3-a7ea-095a4abe9e9c">OFNOTIFYEX</a> structure. 




## -see-also




<a href="https://msdn.microsoft.com/7f3de96f-68d8-4f40-b74f-304835f9def2">CDN_FILEOK</a>



<a href="https://msdn.microsoft.com/864ab80d-cd99-4dd6-8aff-49beed246e53">CDN_FOLDERCHANGE</a>



<a href="https://msdn.microsoft.com/18ee86b2-3446-4de4-a47a-2e44e677f4f7">CDN_HELP</a>



<a href="https://msdn.microsoft.com/337fccac-5444-442d-92f0-862c5302fa21">CDN_INITDONE</a>



<a href="https://msdn.microsoft.com/e622babf-7024-45c5-a8db-f80896f69140">CDN_SELCHANGE</a>



<a href="https://msdn.microsoft.com/a62ca550-0997-4379-aaaf-a5bc9414bd69">CDN_SHAREVIOLATION</a>



<a href="https://msdn.microsoft.com/fb8324db-e435-4ef2-aac5-506a6b7adb2c">CDN_TYPECHANGE</a>



<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/0efe3e60-b300-49c3-a7ea-095a4abe9e9c">OFNOTIFYEX</a>



<a href="https://msdn.microsoft.com/c84932c8-c960-4606-bdec-bc9111c92b54">OPENFILENAME</a>



<b>Reference</b>
 

 

