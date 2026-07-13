---
UID: NF:ole2.OleSave
title: OleSave function (ole2.h)
description: Saves an object opened in transacted mode into the specified storage object.
helpviewer_keywords: ["OleSave","OleSave function [COM]","_ole_OleSave","com.olesave","ole2/OleSave"]
old-location: com\olesave.htm
tech.root: com
ms.assetid: b8d8e1af-05a3-42f5-8672-910a2606e613
ms.date: 12/05/2018
ms.keywords: OleSave, OleSave function [COM], _ole_OleSave, com.olesave, ole2/OleSave
req.header: ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleSave
 - ole2/OleSave
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleSave
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# OleSave function


## -description

Saves an object opened in transacted mode into the specified storage object.

## -parameters

### -param pPS [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a> interface on the object to be saved.

### -param pStg [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the destination storage object to which the object indicated in <i>pPS</i> is to be saved.

### -param fSameAsLoad [in]

<b>TRUE</b> indicates that <i>pStg</i> is the same storage object from which the object was loaded or created; <b>FALSE</b> indicates that <i>pStg</i> was loaded or created from a different storage object.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STGMEDIUM_E_FULL</b></dt>
</dl>
</td>
<td width="60%">
The object could not be saved due to lack of disk space.

This function can also return any of the error values returned by the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a> method.

</td>
</tr>
</table>

## -remarks

The <b>OleSave</b> helper function handles the common situation in which an object is open in transacted mode and is then to be saved into the specified storage object which uses the OLE-provided compound file implementation. Transacted mode means that changes to the object are buffered until either of the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a> or <a href="/windows/desktop/api/objidl/nf-objidl-istorage-revert">IStorage::Revert</a> is called. Callers can handle other situations by calling the <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a> and <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interfaces directly.



<b>OleSave</b> does the following: 

<ul>
<li>Calls the <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">IPersist::GetClassID</a> method to get the CLSID of the object.</li>
<li>Writes the CLSID to the storage object using the <a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstg">WriteClassStg</a> function. 
</li>
<li>Calls the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a> method to save the object.
</li>
<li>If there were no errors on the save; calls the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a> method to commit the changes.
</li>
</ul>
<div class="alert"><b>Note</b>  Static objects are saved into a stream called CONTENTS. Static metafile objects get saved in "placeable metafile format" and static DIB data gets saved in "DIB file format." These formats are defined to be the OLE standards for metafile and DIB. All data transferred using an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface or a file (that is, via <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdatahere">IDataObject::GetDataHere</a>) must be in these formats. Also, all objects whose default file format is a metafile or DIB must write their data into a CONTENTS stream using these standard formats.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>
