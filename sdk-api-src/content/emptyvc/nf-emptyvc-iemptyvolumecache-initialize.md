---
UID: NF:emptyvc.IEmptyVolumeCache.Initialize
title: IEmptyVolumeCache::Initialize (emptyvc.h)
description: Initializes the disk cleanup handler, based on the information stored under the specified registry key.
helpviewer_keywords: ["EVCF_DONTSHOWIFZERO","EVCF_ENABLEBYDEFAULT","EVCF_ENABLEBYDEFAULT_AUTO","EVCF_HASSETTINGS","EVCF_OUTOFDISKSPACE","EVCF_REMOVEFROMLIST","EVCF_SETTINGSMODE","IEmptyVolumeCache interface [Legacy Windows Environment Features]","Initialize method","IEmptyVolumeCache.Initialize","IEmptyVolumeCache::Initialize","Initialize","Initialize method [Legacy Windows Environment Features]","Initialize method [Legacy Windows Environment Features]","IEmptyVolumeCache interface","These flags can be passed by the handler back to the disk cleanup manager:","These flags can be passed in to the object:","_win32_IEmptyVolumeCache_Initialize","emptyvc/IEmptyVolumeCache::Initialize","lwef.iemptyvolumecache_initialize","shell.iemptyvolumecache_initialize"]
old-location: lwef\iemptyvolumecache_initialize.htm
tech.root: lwef
ms.assetid: e0d66c58-6963-4694-984f-6f4a710d08c0
ms.date: 12/05/2018
ms.keywords: EVCF_DONTSHOWIFZERO, EVCF_ENABLEBYDEFAULT, EVCF_ENABLEBYDEFAULT_AUTO, EVCF_HASSETTINGS, EVCF_OUTOFDISKSPACE, EVCF_REMOVEFROMLIST, EVCF_SETTINGSMODE, IEmptyVolumeCache interface [Legacy Windows Environment Features],Initialize method, IEmptyVolumeCache.Initialize, IEmptyVolumeCache::Initialize, Initialize, Initialize method [Legacy Windows Environment Features], Initialize method [Legacy Windows Environment Features],IEmptyVolumeCache interface, These flags can be passed by the handler back to the disk cleanup manager:, These flags can be passed in to the object:, _win32_IEmptyVolumeCache_Initialize, emptyvc/IEmptyVolumeCache::Initialize, lwef.iemptyvolumecache_initialize, shell.iemptyvolumecache_initialize
req.header: emptyvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEmptyVolumeCache::Initialize
 - emptyvc/IEmptyVolumeCache::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEmptyVolumeCache.Initialize
---

# IEmptyVolumeCache::Initialize


## -description

Initializes the disk cleanup handler, based on the information stored under the specified registry key.

## -parameters

### -param hkRegKey [in]

Type: <b>HKEY</b>

A handle to the registry key that holds the information about the handler object.

### -param pcwszVolume [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string with the volume root—for example, "C:\".

### -param ppwszDisplayName [out]

Type: <b>LPWSTR*</b>

A pointer to a null-terminated Unicode string with the name that will be displayed in the disk cleanup manager's list of handlers. If no value is assigned, the registry value will be used.

### -param ppwszDescription [out]

Type: <b>LPWSTR*</b>

A pointer to a null-terminated Unicode string that will be displayed when this object is selected from the disk cleanup manager's list of available disk cleanup handlers. If no value is assigned, the registry value will be used.

### -param pdwFlags [in, out]

Type: <b>DWORD*</b>

The flags that are used to pass information to the handler and back to the disk cleanup manager. 



#### These flags can be passed in to the object:



#### EVCF_OUTOFDISKSPACE

If this flag is set, the user is out of disk space on the drive. When this flag is received, the handler should be aggressive about freeing disk space, even if it results in a performance loss. The handler, however, should not delete files that would cause an application to fail, or the user to lose data.



#### EVCF_SETTINGSMODE

If the disk cleanup manager is being run on a schedule, it will set this flag. You must assign values to the <i>ppwszDisplayName</i> and <i>ppwszDescription</i> parameters. If this flag is set, the disk cleanup manager will not call <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused">IEmptyVolumeCache::GetSpaceUsed</a>, <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-purge">IEmptyVolumeCache::Purge</a>, or <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-showproperties">IEmptyVolumeCache::ShowProperties</a>. Because <b>IEmptyVolumeCache::Purge</b> will not be called, cleanup must be handled by <b>IEmptyVolumeCache::Initialize</b>. The handler should ignore the <i>pcwszVolume</i> parameter and clean up any unneeded files regardless of what drive they are on. Because there is no opportunity for user feedback, only those files that are extremely safe to clean up should be touched.



#### These flags can be passed by the handler back to the disk cleanup manager:



#### EVCF_DONTSHOWIFZERO

Set this flag when there are no files to delete. When <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused">IEmptyVolumeCache::GetSpaceUsed</a> is called, set the <i>pdwSpaceUsed</i> parameter to zero, and the disk cleanup manager will omit the handler from its list. 



#### EVCF_ENABLEBYDEFAULT

Set this flag to have the handler checked by default in the cleanup manager's list. It will run every time the Disk Cleanup utility runs, unless the user clears the handler's check box. Once the check box has been cleared, the handler will not be run until the user selects it again. 



#### EVCF_ENABLEBYDEFAULT_AUTO

Set this flag to have the handler run automatically during scheduled cleanup. This flag should only be set when deletion of the files is low-risk. As with <b>EVCF_ENABLEBYDEFAULT</b>, the user can choose not to run the handler by clearing its check box in the disk cleanup manager's list. 



#### EVCF_HASSETTINGS

Set this flag to indicate that the handler can display a UI. An example of a simple UI is a list box that displays the deletable files and allows the user to select which ones to delete. The disk cleanup manager will then display a button below the cleanup handler's description. The user clicks this button to request the UI. The default button text is "Settings", but the handler can specify a different text by setting the AdvancedButtonText value in its registry key. 



#### EVCF_REMOVEFROMLIST

Set this flag to remove the handler from the disk cleanup manager's list. All registry information will be deleted, and the handler cannot be run again until the key and its values are restored. This flag is used primarily for one-time cleanup operations.

## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no files to delete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The cleanup operation was ended prematurely.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The cleanup operation failed.

</td>
</tr>
</table>

## -remarks

This method is used by the Windows 98 disk cleanup manager. Windows 2000 uses the <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex">InitializeEx</a> method exported by <a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache2">IEmptyVolumeCache2</a>. 

Use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> to allocate memory for the strings returned through <i>ppwszDisplayName</i> and <i>ppwszDescription</i>. The disk cleanup manager will free the memory when it is no longer needed.