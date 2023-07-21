---
UID: NF:sbe.IStreamBufferConfigure.SetDirectory
title: IStreamBufferConfigure::SetDirectory (sbe.h)
description: The SetDirectory method sets the directory where backing files are saved.
helpviewer_keywords: ["IStreamBufferConfigure interface [Microsoft TV Technologies]","SetDirectory method","IStreamBufferConfigure.SetDirectory","IStreamBufferConfigure::SetDirectory","IStreamBufferConfigureSetDirectory","SetDirectory","SetDirectory method [Microsoft TV Technologies]","SetDirectory method [Microsoft TV Technologies]","IStreamBufferConfigure interface","mstv.istreambufferconfigure_setdirectory","sbe/IStreamBufferConfigure::SetDirectory"]
old-location: mstv\istreambufferconfigure_setdirectory.htm
tech.root: mstv
ms.assetid: ff0604d4-bbcd-409e-8e3d-a132218dc3a9
ms.date: 12/05/2018
ms.keywords: IStreamBufferConfigure interface [Microsoft TV Technologies],SetDirectory method, IStreamBufferConfigure.SetDirectory, IStreamBufferConfigure::SetDirectory, IStreamBufferConfigureSetDirectory, SetDirectory, SetDirectory method [Microsoft TV Technologies], SetDirectory method [Microsoft TV Technologies],IStreamBufferConfigure interface, mstv.istreambufferconfigure_setdirectory, sbe/IStreamBufferConfigure::SetDirectory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferConfigure::SetDirectory
 - sbe/IStreamBufferConfigure::SetDirectory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure.SetDirectory
---

# IStreamBufferConfigure::SetDirectory


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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
The <a href="/previous-versions/windows/desktop/mstv/streambufferconfig-object">StreamBufferConfig</a> object was not initialized.

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

Before calling this method, call <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferinitialize-sethkey">IStreamBufferInitialize::SetHKEY</a> to specify a registry key where the information will be stored.

The specified directory is used to store backing files. If no directory is specified, the files are saved in a hidden system directory inside the Temp directory. This directory is not used to store files created by <a href="/previous-versions/windows/desktop/mstv/recording-object">Recording</a> objects; those files are stored in a directory specified by the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink-createrecorder">IStreamBufferSink::CreateRecorder</a> method.

Backing files are created as hidden sytem files.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure">IStreamBufferConfigure Interface</a>