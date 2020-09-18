---
UID: NF:vsbackup.IVssWMComponent.GetDatabaseFile
title: IVssWMComponent::GetDatabaseFile (vsbackup.h)
description: The GetDatabaseFile method obtains an IVssWMFiledesc object containing information about the specified database backup component file.
helpviewer_keywords: ["GetDatabaseFile","GetDatabaseFile method [VSS]","GetDatabaseFile method [VSS]","IVssWMComponent interface","IVssWMComponent interface [VSS]","GetDatabaseFile method","IVssWMComponent.GetDatabaseFile","IVssWMComponent::GetDatabaseFile","_win32_ivsswmcomponent_getdatabasefile","base.ivsswmcomponent_getdatabasefile","vsbackup/IVssWMComponent::GetDatabaseFile"]
old-location: base\ivsswmcomponent_getdatabasefile.htm
tech.root: base
ms.assetid: adb2d6f7-592c-403d-92c0-6b99e2180a6b
ms.date: 12/05/2018
ms.keywords: GetDatabaseFile, GetDatabaseFile method [VSS], GetDatabaseFile method [VSS],IVssWMComponent interface, IVssWMComponent interface [VSS],GetDatabaseFile method, IVssWMComponent.GetDatabaseFile, IVssWMComponent::GetDatabaseFile, _win32_ivsswmcomponent_getdatabasefile, base.ivsswmcomponent_getdatabasefile, vsbackup/IVssWMComponent::GetDatabaseFile
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssWMComponent::GetDatabaseFile
 - vsbackup/IVssWMComponent::GetDatabaseFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssWMComponent.GetDatabaseFile
---

# IVssWMComponent::GetDatabaseFile


## -description

The 
<b>GetDatabaseFile</b> method obtains an 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object containing information about the specified database backup component file.

## -parameters

### -param iDBFile [in]

Offset between 0 and <i>n</i>-1, where <i>n</i> is the number of database files as specified by the <b>cDatabases</b> member of the 
<a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a> object returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getcomponentinfo">IVssWMComponent::GetComponentInfo</a>.

### -param ppFiledesc [out]

Doubly indirect pointer to an 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object containing the returned file descriptor information.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned a pointer to an instance of the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified database file does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

The caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release system resources held by the returned 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a>