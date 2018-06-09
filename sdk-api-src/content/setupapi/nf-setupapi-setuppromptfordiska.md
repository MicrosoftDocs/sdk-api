---
UID: NF:setupapi.SetupPromptForDiskA
title: SetupPromptForDiskA function
author: windows-sdk-content
description: The SetupPromptForDisk function displays a dialog box that prompts the user for a disk.
old-location: setup\setuppromptfordisk.htm
old-project: SetupApi
ms.assetid: 65ccd3d1-1846-48cb-9fe6-ab5c69845e01
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: SetupPromptForDisk, SetupPromptForDisk function [Setup API], SetupPromptForDiskA, SetupPromptForDiskW, _setupapi_setuppromptfordisk, setup.setuppromptfordisk, setupapi/SetupPromptForDisk, setupapi/SetupPromptForDiskA, setupapi/SetupPromptForDiskW
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
req.unicode-ansi: SetupPromptForDiskW (Unicode) and SetupPromptForDiskA (ANSI)
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
 - SetupPromptForDisk
 - SetupPromptForDiskA
 - SetupPromptForDiskW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupPromptForDiskA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupPromptForDisk</b> function displays a dialog box that prompts the user for a disk.


## -parameters




### -param hwndParent [in]

Handle to the parent window for this dialog box.


### -param DialogTitle [in]

Optional pointer to a <b>null</b>-terminated string specifying the dialog title. If this parameter is <b>NULL</b>, the default of ""%s--Files Needed"" (localized) is used. The "%s" is replaced with the text retrieved from the parent window. If no text is retrieved from the parent window, the title is "Files Needed".


### -param DiskName [in]

Optional pointer to a <b>null</b>-terminated string specifying the name of the disk to insert. If this parameter is <b>NULL</b>, the default "(Unknown)" (localized) is used.


### -param PathToSource [in]

Optional pointer to a <b>null</b>-terminated string specifying the path part of the expected location of the file, for example, F:\x86. If not specified, the path where <b>SetupPromptForDisk</b> most recently  located a file is used. If that list is empty, a system default is used.



### -param FileSought [in]

Pointer to a <b>null</b>-terminated string specifying the name of the file needed (filename part only). The filename is displayed if the user clicks on the <b>Browse</b> button. This routine looks for the file using its compressed form names; therefore, you can pass cmd.exe and not worry that the file actually exists as cmd.ex_ on the source media.


### -param TagFile [in]

Optional pointer to a <b>null</b>-terminated string specifying a tag file (filename part only) that identifies the presence of a particular removable media volume. If the currently selected path would place the file on removable media and a tag file is specified, 
<b>SetupPromptForDisk</b> looks for the tag file at the root of the drive to determine whether to continue. 




For example, if <i>PathToSource</i> is A:\x86, the tagfile is disk1.tag, and the user types B:\x86 into the edit control of the prompt dialog box, the routine looks for B:\disk1.tag to determine whether to continue. If the tag file is not found, the function looks for the tagfile using <i>PathToSource</i>.

If a tag file is not specified, removable media works just like non-removable media and <i>FileSought</i> is looked for before continuing.


### -param DiskPromptStyle [in]

Specifies the behavior of the dialog box. This parameter can be a combination of the following flags. 







#### IDF_CHECKFIRST

Check for the file/disk before displaying the prompt dialog box, and, if present, return DPROMPT_SUCCESS immediately.



#### IDF_NOBEEP

Prevent the dialog box from beeping to get the user's attention when it first appears.



#### IDF_NOBROWSE

Do not display the browse option.



#### IDF_NOCOMPRESSED

Do not check for compressed versions of the source file.



#### IDF_NODETAILS

Do not display detail information.



#### IDF_NOFOREGROUND

Prevent the dialog box from becoming the foreground window.



#### IDF_NOSKIP

Do not display the skip option.



#### IDF_OEMDISK

Prompt for a disk supplied by a hardware manufacturer.



#### IDF_WARNIFSKIP

Warn the user that skipping a file may affect the installation.


### -param PathBuffer [in, out]

Optional pointer to a buffer that, upon return, receives the path (no filename) of the location specified by the user through the dialog box.  You should use a <b>null</b>-terminated string. The <b>null</b>-terminated string should not exceed the size of the destination buffer. You can call the function once to get the required buffer size, allocate the necessary memory, and then call the function a second time to retrieve the data. Using this technique, you can avoid errors due to an insufficient buffer size.  See the Remarks section. 



### -param PathBufferSize [in]

Size of the buffer pointed to by <i>PathBuffer</i>, in characters. It should be at least MAX_PATH long. This includes the <b>null</b> terminator. 


### -param PathRequiredSize [in, out]

Optional pointer to a variable that receives the required size for <i>PathBuffer</i>, in characters. This includes the <b>null</b> terminator. 


## -returns



The function returns one of the following values.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If this function is called with a <i>PathBuffer</i> of <b>NULL</b> and a <i>PathBufferSize</i> of zero, the function puts the buffer size needed to hold the specified data into the variable pointed to by <i>PathRequiredSize</i>. If the function succeeds in this, the return value is NO_ERROR. Otherwise, the return value is one of the values described in the Return Values section.






## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/bda8ffef-f1a7-474c-9ec6-f76c2f006d51">SetupCopyError</a>



<a href="https://msdn.microsoft.com/200e1926-7ebd-4373-803d-1c054db5df8d">SetupDeleteError</a>



<a href="https://msdn.microsoft.com/43371fa0-d7b4-42e0-a94d-d307a7210618">SetupRenameError</a>
 

 

