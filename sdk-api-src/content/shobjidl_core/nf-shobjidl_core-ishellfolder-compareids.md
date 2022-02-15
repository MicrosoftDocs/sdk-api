---
UID: NF:shobjidl_core.IShellFolder.CompareIDs
title: IShellFolder::CompareIDs (shobjidl_core.h)
description: Determines the relative order of two file objects or folders, given their item identifier lists.
helpviewer_keywords: ["CompareIDs","CompareIDs method [Windows Shell]","CompareIDs method [Windows Shell]","IShellFolder interface","CompareIDs method [Windows Shell]","IShellFolder2 interface","IShellFolder interface [Windows Shell]","CompareIDs method","IShellFolder.CompareIDs","IShellFolder2 interface [Windows Shell]","CompareIDs method","IShellFolder2::CompareIDs","IShellFolder::CompareIDs","SHCIDS_ALLFIELDS","SHCIDS_CANONICALONLY","_win32_IShellFolder_CompareIDs","shell.IShellFolder_CompareIDs","shobjidl_core/IShellFolder2::CompareIDs","shobjidl_core/IShellFolder::CompareIDs"]
old-location: shell\IShellFolder_CompareIDs.htm
tech.root: shell
ms.assetid: 54d805cc-5396-4892-9347-cafc2d90779f
ms.date: 12/05/2018
ms.keywords: CompareIDs, CompareIDs method [Windows Shell], CompareIDs method [Windows Shell],IShellFolder interface, CompareIDs method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],CompareIDs method, IShellFolder.CompareIDs, IShellFolder2 interface [Windows Shell],CompareIDs method, IShellFolder2::CompareIDs, IShellFolder::CompareIDs, SHCIDS_ALLFIELDS, SHCIDS_CANONICALONLY, _win32_IShellFolder_CompareIDs, shell.IShellFolder_CompareIDs, shobjidl_core/IShellFolder2::CompareIDs, shobjidl_core/IShellFolder::CompareIDs
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolder::CompareIDs
 - shobjidl_core/IShellFolder::CompareIDs
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
 - IShellFolder.CompareIDs
 - IShellFolder2.CompareIDs
---

# IShellFolder::CompareIDs


## -description

Determines the relative order of two file objects or folders, given their item identifier lists.

## -parameters

### -param lParam [in]

Type: <b>LPARAM</b>

A value that specifies how the comparison should be performed. 

					

The lower sixteen bits of <i>lParam</i> define the sorting rule. Most applications set the sorting rule to the default value of zero, indicating that the two items should be compared by name. The system does not define any other sorting rules. Some folder objects might allow calling applications to use the lower sixteen bits of <i>lParam</i> to specify folder-specific sorting rules. The rules and their associated <i>lParam</i> values are defined by the folder.

When the system folder view object calls <b>IShellFolder::CompareIDs</b>, the lower sixteen bits of <i>lParam</i> are used to specify the column to be used for the comparison.

The upper sixteen bits of <i>lParam</i> are used for flags that modify the sorting rule. The system currently defines these modifier flags.



#### SHCIDS_ALLFIELDS


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. Compare all the information contained in the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure, not just the display names. This flag is valid only for folder objects that support the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a> interface. For instance, if the two items are files, the folder should compare their names, sizes, file times, attributes, and any other information in the structures. If this flag is set, the lower sixteen bits of <i>lParam</i> must be zero.



#### SHCIDS_CANONICALONLY


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. When comparing by name, compare the system names but not the display names. When this flag is passed, the two items are compared by whatever criteria the Shell folder determines are most efficient, as long as it implements a consistent sort function. This flag is useful when comparing for equality or when the results of the sort are not displayed to the user. This flag cannot be combined with other flags.

### -param pidl1 [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to the first item's <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure. It will be relative to the folder. This <b>ITEMIDLIST</b> structure can contain more than one element; therefore, the entire structure must be compared, not just the first element.

### -param pidl2 [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to the second item's <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure. It will be relative to the folder. This <b>ITEMIDLIST</b> structure can contain more than one element; therefore, the entire structure must be compared, not just the first element.

## -returns

Type: <b>HRESULT</b>

If this method is successful, the CODE field of the <b>HRESULT</b> contains one of the following values. For information regarding the extraction of the CODE field from the returned <b>HRESULT</b>, see Remarks. If this method is unsuccessful, it returns a COM error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Negative</b></dt>
</dl>
</td>
<td width="60%">
A negative return value indicates that the first item should precede the second (pidl1 &lt; pidl2).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Positive</b></dt>
</dl>
</td>
<td width="60%">
A positive return value indicates that the first item should follow the second (pidl1 &gt; pidl2).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Zero</b></dt>
</dl>
</td>
<td width="60%">
A return value of zero indicates that the two items are the same (pidl1 = pidl2).

</td>
</tr>
</table>

## -remarks

<h3><a id="Note_to_Calling_Applications"></a><a id="note_to_calling_applications"></a><a id="NOTE_TO_CALLING_APPLICATIONS"></a>Note to Calling Applications</h3>
Do not set the <b>SHCIDS_ALLFIELDS</b> flag in <i>lParam</i> if the folder object does not support <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>. Doing so might have unpredictable results. If you use the <b>SHCIDS_ALLFIELDS</b> flag, the lower sixteen bits of <i>lParam</i> must be set to zero.

Use the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_code">HRESULT_CODE</a> macro to extract the CODE field from the <b>HRESULT</b>, then cast the result as a <b>short</b>.
		
    			


```cpp
HRESULT hres = psf->CompareIDs(lParam, pidl1, pidl2);
if ((short)HRESULT_CODE(hres) < 0)
   { /* pidl1 comes first */ }
else if ((short)HRESULT_CODE(hres) > 0) 
   { /* pidl2 comes first */ }
else 
   { /* the two pidls are equal */ }

```


<h3><a id="Note_to_Implementers"></a><a id="note_to_implementers"></a><a id="NOTE_TO_IMPLEMENTERS"></a>Note to Implementers</h3>
To extract the sorting rule, use a bitwise AND operator (&amp;) to combine <i>lParam</i> with SHCIDS_COLUMNMASK (0X0000FFFF). This operation masks off the upper sixteen bits of <i>lParam</i>, including the <b>SHCIDS_ALLFIELDS</b> value.

The <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult">MAKE_HRESULT</a> macro is useful for constructing the return value for
            an implementation of the CompareIDs method.  For example:
			
    			


```cpp
HRESULT CompareIDs(LPARAM lParam, PCUIDLIST_RELATIVE pidl1, PCUIDLIST_RELATIVE pidl2)
{
    short sResult;
    unsigned uSeverity = 0x000000000;
    
    // Code that determines the relative order of pidl1 and pidl2 according to
    // any sorting rules specified by lParam goes here.
    //
    // Set sResult = -1 if pidl1 precedes pidl2 (pidl1 < pidl2).
    // Set sResult =  1 if pidl1 follows pidl2. (pidl1 > pidl2).
    // Set sResult =  0 if pidl1 and pidl2 are equivalent in terms of ordering. (pidl1 = pidl2).
    //
    // Leave uSeverity = 0 if the order is successfully determined.
    // Set uSeverity = 0x00000001 if there is an error.

    return MAKE_HRESULT(uSeverity, 0, (unsigned short)sResult);
}

```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>