---
UID: NF:comadmin.ICOMAdminCatalog2.DumpApplicationInstance
title: ICOMAdminCatalog2::DumpApplicationInstance (comadmin.h)
description: Creates a dump file containing an image of the state of the specified application instance (process).
helpviewer_keywords: ["DumpApplicationInstance","DumpApplicationInstance method [COM+]","DumpApplicationInstance method [COM+]","ICOMAdminCatalog2 interface","ICOMAdminCatalog2 interface [COM+]","DumpApplicationInstance method","ICOMAdminCatalog2.DumpApplicationInstance","ICOMAdminCatalog2::DumpApplicationInstance","_cos_icomadmincatalog2_DumpApplicationInstance","comadmin/ICOMAdminCatalog2::DumpApplicationInstance","cos.icomadmincatalog2_dumpapplicationinstance"]
old-location: cos\icomadmincatalog2_dumpapplicationinstance.htm
tech.root: cos
ms.assetid: 76c121c6-4ba6-49da-93dc-9094acb1994c
ms.date: 12/05/2018
ms.keywords: DumpApplicationInstance, DumpApplicationInstance method [COM+], DumpApplicationInstance method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],DumpApplicationInstance method, ICOMAdminCatalog2.DumpApplicationInstance, ICOMAdminCatalog2::DumpApplicationInstance, _cos_icomadmincatalog2_DumpApplicationInstance, comadmin/ICOMAdminCatalog2::DumpApplicationInstance, cos.icomadmincatalog2_dumpapplicationinstance
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ICOMAdminCatalog2::DumpApplicationInstance
 - comadmin/ICOMAdminCatalog2::DumpApplicationInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.DumpApplicationInstance
---

# ICOMAdminCatalog2::DumpApplicationInstance


## -description

Creates a dump file containing an image of the state of the specified application instance (process).
<div class="alert"><b>Note</b>  As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</div><div> </div>

## -parameters

### -param bstrApplicationInstanceID [in]

The GUID of the application instance.

### -param bstrDirectory [in]

The complete path to the directory into which the dump file is placed. Do not include the file name. If this parameter is <b>NULL</b>, the default directory is %SystemRoot%\system32\com\dmp.

### -param lMaxImages [in]

The maximum number of dump files that may exist in the dump directory. Specifying this variable prevents dump files from consuming too much storage space.

### -param pbstrDumpFile [out, retval]

The name of the dump file containing the resulting application instance image.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_APP_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The specified process is not running.


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>