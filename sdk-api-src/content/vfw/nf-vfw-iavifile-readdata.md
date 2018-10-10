---
UID: NF:vfw.IAVIFile.ReadData
title: IAVIFile::ReadData
author: windows-sdk-content
description: The ReadData method reads file headers. Called when an application uses the AVIFileReadData function.
old-location: multimedia\iavifile_readdata.htm
tech.root: Multimedia
ms.assetid: 52071d08-1e95-4b4b-b85c-3fcca2c666aa
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IAVIFile interface [Windows Multimedia],ReadData method, IAVIFile.ReadData, IAVIFile::ReadData, ReadData, ReadData method [Windows Multimedia], ReadData method [Windows Multimedia],IAVIFile interface, _win32_IAVIFile_ReadData, multimedia.iavifile_readdata, vfw/IAVIFile::ReadData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vfw.h
req.include-header: 
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
req.lib: Vfw32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IAVIFile.ReadData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIFile::ReadData


## -description



The <b>ReadData</b> method reads file headers. Called when an application uses the <a href="https://msdn.microsoft.com/9eef2ef4-316e-43e8-8011-14f1c0b46d50">AVIFileReadData</a> function.




## -parameters




### -param ckid

TBD


### -param lpData

TBD


### -param lpcbData

TBD




#### - fcc

Four-character code of the header to read.


#### - lpBuffer

Pointer to the buffer for the data.


#### - lpcbBuffer

Size, in bytes, of the buffer specified by <i>lpBuffer</i>. When this method returns control to the application, the contents of this parameter specifies the amount of data read.


#### - ps

Pointer to the interface to a file.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>ReadData</b> has the following syntax:


```cpp

HRESULT ReadData(DWORD fcc, LPVOID lp, LONG *lpcb); 
 

```





## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

