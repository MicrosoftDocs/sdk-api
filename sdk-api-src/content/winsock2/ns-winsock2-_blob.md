---
UID: NS:winsock2._BLOB
title: "_BLOB"
author: windows-sdk-content
description: The BLOB structure, derived from Binary Large Object, contains information about a block of data.
old-location: winsock\blob_2.htm
tech.root: WinSock
ms.assetid: eb1ff7d1-79db-478f-9f3e-48507d333c76
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPBLOB, BLOB, BLOB structure [Winsock], _BLOB, _win32_blob_2, tagBLOB, winsock.blob_2, wtypesbase/BLOB"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winsock2.h
req.include-header: Wtypes.h, Nspapi.h, Winsock2.h, Wtypes.h, Nspapi.h, Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wtypesbase.h
api_name:
 - BLOB
product: Windows
targetos: Windows
req.typenames: BLOB, *LPBLOB
req.redist: 
---

# _BLOB structure


## -description


The 
<b>BLOB</b> structure, derived from Binary Large Object, contains information about a block of data.


## -struct-fields




### -field cbSize

Size of the block of data pointed to by <b>pBlobData</b>, in bytes.


### -field pBlobData.size_is

 


### -field pBlobData.size_is.cbSize

 


### -field pBlobData

Pointer to a block of data.


## -remarks



The structure name 
<b>BLOB</b> comes from the acronym BLOB, which stands for Binary Large Object.

This structure does not describe the nature of the data pointed to by <b>pBlobData</b>.

<div class="alert"><b>Note</b>  Windows Sockets defines a similar 
<b>BLOB</b> structure in Wtypes.h. Using both header files in the same source code file creates redefinition–compile time errors.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d71f3661-0efb-4376-966c-fb5c340ce1c5">Bluetooth and BLOB</a>



<a href="https://msdn.microsoft.com/e76e0c1b-8cbf-45ad-a685-fb672801c24d">SERVICE_INFO</a>
 

 

