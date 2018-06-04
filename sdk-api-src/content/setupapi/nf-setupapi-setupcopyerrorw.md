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

# SetupCopyErrorW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCopyError</b> function generates a dialog box to notify a user of a copy file error.


## -parameters




### -param hwndParent [in]

The handle to the parent window for this dialog box.


### -param DialogTitle [in]

An optional pointer to a <b>null</b>-terminated string that specifies the dialog box title. 

This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the default title of "Copy Error" (localized to the system language) is used.


### -param DiskName [in]

An optional pointer to a <b>null</b>-terminated string that specifies the name of the disk to insert.  

This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the default name "(Unknown)" (localized to the system language) is used.


### -param PathToSource [in]

A pointer to the path component of the source file where an operation fails, for example, F:\x86. 

Use a <b>null</b>-terminated string. 


### -param SourceFile [in]

A pointer to a <b>null</b>-terminated string that specifies the filename part of the file where an operation fails. 

Use a <b>null</b>-terminated string. This filename is displayed if the user clicks on the <b>Details</b> or <b>Browse</b> buttons. The <b>SetupCopyError</b> function looks for the file that uses its compressed form names. Therefore, you can pass cmd.exe and not worry that the file actually exists as cmd.ex_ on the source media. 



### -param TargetPathFile [in]

An optional pointer to a <b>null</b>-terminated string that specifies the full path of the target file for rename and copy operations. 

Use a <b>null</b>-terminated string.  This parameter can be <b>NULL</b>. If TargetPathFile is not specified, "(Unknown)" (localized to the system language) is used.


### -param Win32ErrorCode [out]

If an error occurs, this member is the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Code</a>. 

If an error does not occur, it is  NO_ERROR.


### -param Style [in]

The flags that control display formatting and behavior of a dialog box. 

This parameter can be one of the following flags.





#### IDF_NOBROWSE

Do not display the browse option.



#### IDF_NOSKIP

Do not display the skip file option.



#### IDF_NODETAILS

Do not display the details option. 

If this flag is set, the <i>TargetPathFile</i> and <i>Win32ErrorCode</i> parameters can be omitted.



#### IDF_NOCOMPRESSED

Do not check for compressed versions of the source file.



#### IDF_OEMDISK

The operation source is a disk that a hardware manufacturer provides.



#### IDF_NOBEEP

Prevents the dialog box from beeping to get the user's attention when it first appears.



#### IDF_NOFOREGROUND

Prevents the dialog box from becoming the foreground window.



#### IDF_WARNIFSKIP

Warns the user that skipping a file can affect the installation.


### -param PathBuffer [in, out]

An optional pointer to a variable in which this function returns the path (not including the filename) of the location that a user specifies in the dialog box. You should use a null-terminated string. 

The <b>null</b>-terminated string should not exceed the size of the destination buffer. To avoid insufficient buffer errors, <i>PathBuffer</i> should be at least MAX_PATH.
For more information, see the Remarks section of this topic.


### -param PathBufferSize [in]

 The size of the buffer that  <i>PathBuffer</i> points to, in characters. 

The buffer size should be at least MAX_PATH characters, including the <b>null</b> terminator.


### -param PathRequiredSize [in, out]

An optional pointer to a variable in which this function returns the required buffer size, in characters, including the <b>null</b> terminator. 


##### - Style.IDF_NOBEEP

Prevents the dialog box from beeping to get the user's attention when it first appears.


##### - Style.IDF_NOBROWSE

Do not display the browse option.


##### - Style.IDF_NOCOMPRESSED

Do not check for compressed versions of the source file.


##### - Style.IDF_NODETAILS

Do not display the details option. 

If this flag is set, the <i>TargetPathFile</i> and <i>Win32ErrorCode</i> parameters can be omitted.


##### - Style.IDF_NOFOREGROUND

Prevents the dialog box from becoming the foreground window.


##### - Style.IDF_NOSKIP

Do not display the skip file option.


##### - Style.IDF_OEMDISK

The operation source is a disk that a hardware manufacturer provides.


##### - Style.IDF_WARNIFSKIP

Warns the user that skipping a file can affect the installation.


## -returns



The function returns one of the following values.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If this function is called with a <i>PathBuffer</i> of <b>NULL</b> and a <i>PathBufferSize</i> of 0 (zero), the function puts the buffer size that is needed to hold the specified data into the variable pointed to by <i>PathRequiredSize</i>. 

If the function succeeds, the return value is NO_ERROR. Otherwise, the return value is one of the specified values.

To avoid insufficient buffer errors, <i>ReturnBuffer</i> should be at least MAX_PATH.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/200e1926-7ebd-4373-803d-1c054db5df8d">SetupDeleteError</a>



<a href="https://msdn.microsoft.com/65ccd3d1-1846-48cb-9fe6-ab5c69845e01">SetupPromptForDisk</a>



<a href="https://msdn.microsoft.com/43371fa0-d7b4-42e0-a94d-d307a7210618">SetupRenameError</a>
 

 

