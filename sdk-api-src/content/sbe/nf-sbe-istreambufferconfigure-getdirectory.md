---
UID: NF:sbe.IStreamBufferConfigure.GetDirectory
title: IStreamBufferConfigure::GetDirectory
author: windows-sdk-content
description: The GetDirectory method retrieves the directory where backing files are saved.
old-location: mstv\istreambufferconfigure_getdirectory.htm
tech.root: MSTV
ms.assetid: bb5d955d-11da-4ff3-990f-02c0c80d6405
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetDirectory, GetDirectory method [Microsoft TV Technologies], GetDirectory method [Microsoft TV Technologies],IStreamBufferConfigure interface, IStreamBufferConfigure interface [Microsoft TV Technologies],GetDirectory method, IStreamBufferConfigure.GetDirectory, IStreamBufferConfigure::GetDirectory, IStreamBufferConfigureGetDirectory, mstv.istreambufferconfigure_getdirectory, sbe/IStreamBufferConfigure::GetDirectory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure.GetDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferConfigure::GetDirectory


## -description


The <b>GetDirectory</b> method retrieves the directory where backing files are saved.


## -parameters




### -param ppszDirectoryName [out]

Pointer to a variable that receives the fully qualified directory name.


## -returns



Returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The caller must free the returned string by calling <b>CoTaskMemFree</b>.




## -see-also




<a href="https://msdn.microsoft.com/8874fefd-2241-4b04-a7d5-191e13743fa0">IStreamBufferConfigure Interface</a>
 

 

