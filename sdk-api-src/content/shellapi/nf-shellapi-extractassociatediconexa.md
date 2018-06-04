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

# ExtractAssociatedIconExA function


## -description


<p class="CCE_Message">[<b>ExtractAssociatedIconEx</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets a handle to an icon stored as a resource in a file or an icon stored in a file's associated executable file. It extends the <a href="https://msdn.microsoft.com/157ce603-9988-4cae-a2cd-51db290268c3">ExtractAssociatedIcon</a> function by retrieving the icon's ID when that icon is extracted from an executable file.


## -parameters




### -param hInst [in]

Type: <b>HINSTANCE</b>

The handle of the module from which to extract the icon.


### -param pszIconPath

TBD


### -param piIconIndex

TBD


### -param piIconId

TBD




#### - lpIconPath [in, out]

Type: <b>LPTSTR</b>

Pointer to a string that, on entry, specifies the full path and file name of the file that contains the icon. The function extracts the icon handle from that file, or from an executable file associated with that file. 

                    

When this function returns, if the icon handle was obtained from an executable file (either an executable file directly pointed to by this parameter or an associated executable file) the function stores the full path and file name of that executable in the buffer pointed to by this parameter.


#### - lpiIconId [in, out]

Type: <b>LPWORD</b>

Pointer to a <b>WORD</b> value that, on entry, specifies the ID of the icon whose handle is to be obtained.

                    

When the function returns, if the icon handle was obtained from an executable file (either an executable file pointed to by <i>lpIconPath</i> or an associated executable file), this value points to the icon's ID within that file.


#### - lpiIconIndex [in, out]

Type: <b>LPWORD</b>

Pointer to a <b>WORD</b> value that, on entry, specifies the index of the icon whose handle is to be obtained. 

                    

When the function returns, if the icon handle was obtained from an executable file (either an executable file pointed to by <i>lpIconPath</i> or an associated executable file), this value points to the icon's index in that file.


## -returns



Type: <b>HICON</b>

Returns the icon's handle if successful, otherwise <b>NULL</b>.




## -remarks



The icon handle returned by this function must be released by calling <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> when it is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/157ce603-9988-4cae-a2cd-51db290268c3">ExtractAssociatedIcon</a>



<a href="https://msdn.microsoft.com/a0314423-79d6-416e-8be0-be946477da3e">ExtractIcon</a>



<a href="https://msdn.microsoft.com/1c4d760a-79b5-4646-9cf2-6cd32c5d05ee">ExtractIconEx</a>
 

 

