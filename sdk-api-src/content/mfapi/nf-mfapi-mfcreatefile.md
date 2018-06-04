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

# MFCreateFile function


## -description



          Creates a byte stream from a file.
        


## -parameters




### -param AccessMode


            The requested access mode, specified as a member of the <a href="https://msdn.microsoft.com/38108686-5378-4844-8d5a-a433e89f62bb">MF_FILE_ACCESSMODE</a> enumeration.
          


### -param OpenMode


            The behavior of the function if the file already exists or does not exist, specified as a member of the <a href="https://msdn.microsoft.com/0c0e94fa-cbcc-4abc-9020-af6d36a4d3b6">MF_FILE_OPENMODE</a> enumeration.
          


### -param fFlags


            Bitwise <b>OR</b> of values from the <a href="https://msdn.microsoft.com/1e1c906e-c832-4df1-96f5-86e690c3c34e">MF_FILE_FLAGS</a> enumeration.
          


### -param pwszFileURL


            Pointer to a null-terminated string that contains the file name.
          


### -param ppIByteStream


            Receives a pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of the byte stream. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

