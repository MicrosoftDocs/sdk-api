---
UID: NF:msctf.ITfContextOwner.GetStatus
title: ITfContextOwner::GetStatus
author: windows-sdk-content
description: The ITfContextOwner::GetStatus method obtains the status of a document. The document status is returned through the TS_STATUS structure.
old-location: tsf\itfcontextowner_getstatus.htm
tech.root: TSF
ms.assetid: ce30ec8a-48fe-4ec7-a7e1-2a0cf084097d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITfContextOwner interface, ITfContextOwner interface [Text Services Framework],GetStatus method, ITfContextOwner.GetStatus, ITfContextOwner::GetStatus, _tsf_itfcontextowner_getstatus_ref, msctf/ITfContextOwner::GetStatus, tsf.itfcontextowner_getstatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msimtf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwner.GetStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfContextOwner::GetStatus


## -description


The <b>ITfContextOwner::GetStatus</b> method obtains the status of a document. The document status is returned through the <a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS</a> structure.


## -parameters




### -param pdcs [out]

Receives the <a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS</a> structure that contains the document status. Cannot be <b>NULL</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6ed040ac-8584-4f09-9af8-218b5cd33765">ITextStoreACP::GetStatus
      </a>



<a href="https://msdn.microsoft.com/630646df-dd47-4dbf-9787-f9d697ad8d7a">ITfContextOwner</a>



<a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS
      </a>
 

 

