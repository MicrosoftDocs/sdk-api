---
UID: NF:emptyvc.IEmptyVolumeCache2.InitializeEx
title: IEmptyVolumeCache2::InitializeEx (emptyvc.h)
description: Initializes the disk cleanup handler. It provides better support for localization than Initialize.
helpviewer_keywords: ["EVCF_DONTSHOWIFZERO","EVCF_ENABLEBYDEFAULT","EVCF_ENABLEBYDEFAULT_AUTO","EVCF_HASSETTINGS","EVCF_OUTOFDISKSPACE","EVCF_REMOVEFROMLIST","EVCF_SETTINGSMODE","IEmptyVolumeCache2 interface [Legacy Windows Environment Features]","InitializeEx method","IEmptyVolumeCache2.InitializeEx","IEmptyVolumeCache2::InitializeEx","InitializeEx","InitializeEx method [Legacy Windows Environment Features]","InitializeEx method [Legacy Windows Environment Features]","IEmptyVolumeCache2 interface","These flags can be passed by the handler back to the disk cleanup manager:","These flags can be passed in to the object:","_win32_IEmptyVolumeCache2_InitializeEx","emptyvc/IEmptyVolumeCache2::InitializeEx","lwef.iemptyvolumecache2_initializeex","shell.iemptyvolumecache2_initializeex"]
old-location: lwef\iemptyvolumecache2_initializeex.htm
tech.root: lwef
ms.assetid: 42f39dcd-0292-4121-89e9-80145b1c1c7d
ms.date: 12/05/2018
ms.keywords: EVCF_DONTSHOWIFZERO, EVCF_ENABLEBYDEFAULT, EVCF_ENABLEBYDEFAULT_AUTO, EVCF_HASSETTINGS, EVCF_OUTOFDISKSPACE, EVCF_REMOVEFROMLIST, EVCF_SETTINGSMODE, IEmptyVolumeCache2 interface [Legacy Windows Environment Features],InitializeEx method, IEmptyVolumeCache2.InitializeEx, IEmptyVolumeCache2::InitializeEx, InitializeEx, InitializeEx method [Legacy Windows Environment Features], InitializeEx method [Legacy Windows Environment Features],IEmptyVolumeCache2 interface, These flags can be passed by the handler back to the disk cleanup manager:, These flags can be passed in to the object:, _win32_IEmptyVolumeCache2_InitializeEx, emptyvc/IEmptyVolumeCache2::InitializeEx, lwef.iemptyvolumecache2_initializeex, shell.iemptyvolumecache2_initializeex
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
 - IEmptyVolumeCache2::InitializeEx
 - emptyvc/IEmptyVolumeCache2::InitializeEx
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
 - IEmptyVolumeCache2.InitializeEx
---

# IEmptyVolumeCache2::InitializeEx


## -description

Initializes the disk cleanup handler. It provides better support for localization than <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-initialize">Initialize</a>.

## -parameters

### -param hkRegKey [in]

Type: <b>HKEY</b>

A handle to the registry key that holds the information about the handler object.

### -param pcwszVolume [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string with the volume root—for example, "C:\".

### -param pcwszKeyName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string with the name of the handler's registry key.

### -param ppwszDisplayName [out]

Type: <b>LPWSTR*</b>

A pointer to a null-terminated Unicode string with the name that will be displayed in the disk cleanup manager's list of handlers. You must assign a value to this parameter.

### -param ppwszDescription [out]

Type: <b>LPWSTR*</b>

A pointer to a null-terminated Unicode string that will be displayed when this object is selected from the disk cleanup manager's list of available disk cleaners. You must assign a value to this parameter.

### -param ppwszBtnText [out]

Type: <b>LPWSTR*</b>

A pointer to a null-terminated Unicode string with the text that will be displayed on the disk cleanup manager's <b>Settings</b> button. If the <b>EVCF_HASSETTINGS</b> flag is set, you must assign a value to <i>ppwszBtnText</i>. Otherwise, you can set it to <b>NULL</b>.

### -param pdwFlags [in, out]

Type: <b>DWORD*</b>

Flags that are used to pass information to the handler, and back to the disk cleanup manager. 



#### These flags can be passed in to the object:



#### EVCF_OUTOFDISKSPACE

If this flag is set, the user is out of disk space on the drive. When this flag is received, the handler should be aggressive about freeing disk space, even if it results in a performance loss. The handler, however, should not delete files that would cause an application to fail, or the user to lose data.



#### EVCF_SETTINGSMODE

If the disk cleanup manager is run on a schedule, it will set the <b>EVCF_SETTINGSMODE</b> flag. You must assign values to the <i>ppwszDisplayName</i> and <i>ppwszDescription</i> parameters. If this flag is set, the disk cleanup manager will not call <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused">GetSpaceUsed</a>, <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-purge">Purge</a>, or <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-showproperties">ShowProperties</a>. Because <b>Purge</b> will not be called, cleanup must be handled by <b>InitializeEx</b>. The handler should ignore the <i>pcwszVolume</i> parameter and clean up any unneeded files regardless of what drive they are on. Because there is no opportunity for user feedback, only those files that are extremely safe to clean up should be touched.



#### These flags can be passed by the handler back to the disk cleanup manager:



#### EVCF_DONTSHOWIFZERO

Set this flag when there are no files to delete. When <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused">GetSpaceUsed</a> is called, set the <i>pdwSpaceUsed</i> parameter to zero, and the disk cleanup manager will omit the handler from its list.



#### EVCF_ENABLEBYDEFAULT

Set this flag to have the handler checked by default in the disk cleanup manager's list. The handler will be run every time the disk cleanup utility runs, unless the user clears the handler's check box. Once the check box has been cleared, the handler will not be run until the user selects it again.



#### EVCF_ENABLEBYDEFAULT_AUTO

Set this flag to have the handler run automatically during scheduled cleanup. This flag should only be set when deletion of the files is low-risk. As with <b>EVCF_ENABLEBYDEFAULT</b>, the user can choose not to run the handler by clearing its check box in the disk cleanup manager's list.



#### EVCF_HASSETTINGS

Set this flag to indicate that the handler can display a UI. An example of a simple UI is a list box that displays the deletable files and allows the user to select which ones to delete. The disk cleanup manager will then display a button below the cleanup handler's description. The user clicks this button to request the UI. Use the <i>ppwszBtnText</i> parameter to specify the button's text. 




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

The Windows 2000 disk cleanup manager will first call <b>IEmptyVolumeCache2::InitializeEx</b> to initialize a disk cleanup handler. It will only call <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-initialize">Initialize</a> if the <a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache2">IEmptyVolumeCache2</a> interface is not implemented. The Windows 98 disk cleanup manager only supports <b>Initialize</b>.

<b>InitializeEx</b> is intended to provide better localization support than <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-initialize">Initialize</a>. When <b>InitializeEx</b> is called, the handler application must assign appropriately localized values to the <i>ppwszDisplayName</i> and <i>ppwszDescription</i> parameters. If the <b>Settings</b> button is enabled, you must also assign a value to the <i>ppwszBtnText</i> parameter. Unlike <b>Initialize</b>, if you set these strings to <b>NULL</b> to notify the disk cleanup manager to retrieve the default values from the registry, <b>InitializeEx</b> will fail. 

Use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> to allocate memory for the strings returned through <i>ppwszDisplayName</i>, <i>ppwszDescription</i>, and <i>ppwszBtnText</i>. The disk cleanup manager will free the memory when it is no longer needed.