---
UID: NF:sbe.IStreamBufferConfigure.SetDirectory
title: IStreamBufferConfigure::SetDirectory
author: windows-sdk-content
description: The SetDirectory method sets the directory where backing files are saved.
old-location: mstv\istreambufferconfigure_setdirectory.htm
tech.root: mstv
ms.assetid: ff0604d4-bbcd-409e-8e3d-a132218dc3a9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStreamBufferConfigure interface [Microsoft TV Technologies],SetDirectory method, IStreamBufferConfigure.SetDirectory, IStreamBufferConfigure::SetDirectory, IStreamBufferConfigureSetDirectory, SetDirectory, SetDirectory method [Microsoft TV Technologies], SetDirectory method [Microsoft TV Technologies],IStreamBufferConfigure interface, mstv.istreambufferconfigure_setdirectory, sbe/IStreamBufferConfigure::SetDirectory
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
 - IStreamBufferConfigure.SetDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferConfigure::SetDirectory


## -description


The <b>SetDirectory</b> method sets the directory where backing files are saved.


## -parameters




### -param pszDirectoryName [in]

Pointer to a null-terminated string containing the fully qualified directory name. If the specified directory does not exist, it will be created.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/10678f33-2117-4add-8e4b-7b4d4eed11a9">StreamBufferConfig</a> object was not initialized.

</td>
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



Before calling this method, call <a href="https://msdn.microsoft.com/f8d85180-2575-4525-9b8a-bec354e2cd4c">IStreamBufferInitialize::SetHKEY</a> to specify a registry key where the information will be stored.

The specified directory is used to store backing files. If no directory is specified, the files are saved in a hidden system directory inside the Temp directory. This directory is not used to store files created by <a href="https://msdn.microsoft.com/717a3b99-d998-4e64-aab6-6b06e18991da">Recording</a> objects; those files are stored in a directory specified by the <a href="https://msdn.microsoft.com/a9f3b7e1-4f54-4802-af24-4b791ee646fc">IStreamBufferSink::CreateRecorder</a> method.

Backing files are created as hidden sytem files.




## -see-also




<a href="https://msdn.microsoft.com/8874fefd-2241-4b04-a7d5-191e13743fa0">IStreamBufferConfigure Interface</a>
 

 

