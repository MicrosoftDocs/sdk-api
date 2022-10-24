---
UID: NF:propidlbase.IPropertyStorage.Commit
title: IPropertyStorage::Commit (propidlbase.h)
description: The IPropertyStorage::Commit method saves changes made to a property storage object to the parent storage object.
helpviewer_keywords: ["Commit","Commit method [Structured Storage]","Commit method [Structured Storage]","IPropertyStorage interface","IPropertyStorage [Strctd Stg]","Commit","IPropertyStorage interface [Structured Storage]","Commit method","IPropertyStorage.Commit","IPropertyStorage::Commit","_stg_ipropertystorage_commit","propidl/IPropertyStorage::Commit","stg.ipropertystorage_commit"]
old-location: stg\ipropertystorage_commit.htm
tech.root: Stg
ms.assetid: 00efae8b-023e-425d-b7cd-c40c17d7948e
ms.date: 08/02/2022
ms.keywords: Commit, Commit method [Structured Storage], Commit method [Structured Storage],IPropertyStorage interface, IPropertyStorage [Strctd Stg],Commit, IPropertyStorage interface [Structured Storage],Commit method, IPropertyStorage.Commit, IPropertyStorage::Commit, _stg_ipropertystorage_commit, propidl/IPropertyStorage::Commit, stg.ipropertystorage_commit
req.header: propidlbase.h
req.include-header: Objbase.h, Propidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyStorage::Commit
 - propidlbase/IPropertyStorage::Commit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IPropertyStorage.Commit
---

# IPropertyStorage::Commit


## -description

The <b>IPropertyStorage::Commit</b> method saves changes made to a property storage object to the parent storage object.

## -parameters

### -param grfCommitFlags [in]

The flags that specify the conditions under which the commit is to be performed. For more information about specific flags and their meanings, see the Remarks section.

## -returns

This method supports the standard return value E_UNEXPECTED, as well as the following:

## -remarks

Like <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a>, the <b>IPropertyStorage::Commit</b> method ensures that any changes made to a property storage object are reflected in the parent storage.

In direct mode in the compound file implementation, a call to this method causes any changes currently in the memory buffers to be flushed to the underlying property stream. In the compound-file implementation for nonsimple property sets, 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a> is also called on the underlying substorage object with the passed <i>grfCommitFlags</i> parameter.

In transacted mode, this method causes the changes to be permanently reflected in the persistent image of the storage object. The changes that are committed must have been made to this property set since it was opened or since the last commit on this opening of the property set.  The <b>commit</b> method publishes the changes made on one object level to the next level. Of course, this remains subject to any outer-level transaction that may be present on the object in which this property set is contained. Write permission must be specified when the property set is opened (through 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>) on the property set opening for the commit operation to succeed.

If the commit operation fails for any reason, the state of the property storage object remains as it was before the commit.

This call has no effect on existing storage- or stream-valued properties opened from this property storage, but it does commit them.

Valid values for the <i>grfCommitFlags</i> parameter are listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>STGC_DEFAULT</td>
<td>Commits per the usual transaction semantics. Last writer wins. This flag may not be specified with other flag values.</td>
</tr>
<tr>
<td>STGC_ONLYIFCURRENT</td>
<td>Commits the changes only if the current persistent contents of the property set are the ones on which the changes about to be committed are based. That is, does not commit changes if the contents of the property set have been changed by a commit from another opening of the property set. The error STG_E_NOTCURRENT is returned if the commit does not succeed for this reason.</td>
</tr>
<tr>
<td>STGC_OVERWRITE</td>
<td>Useful only when committing a transaction that has no further outer nesting level of transactions, though acceptable in all cases. <div class="alert"><b>Note</b>  Indicates that the caller is willing to risk some data corruption at the expense of decreased disk usage on the destination volume. This flag is potentially useful in low disk-space scenarios, though it should be used with caution.</div>
<div> </div>
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Using <b>IPropertyStorage::Commit</b> to write properties to image files on Windows XP does not work.  Affected image file formats include:<ul>
<li>.bmp</li>
<li>.dib</li>
<li>.emf</li>
<li>.gif</li>
<li>.ico</li>
<li>.jfif</li>
<li>.jpe</li>
<li>.jpeg</li>
<li>.jpg</li>
<li>.png</li>
<li>.rle</li>
<li>.tiff</li>
<li>.wmf</li>
</ul>Due to a bug in the image file property handler on Windows XP, calling <b>IPropertyStorage::Commit</b> actually discards any changes made rather than persisting them.

 

A workaround is to

omit the call to <b>IPropertyStorage::Commit</b>. Calling IUnknown::Release on the XP image file property handler without calling <b>IPropertyStorage::Commit</b> first implicitly commits the changes to the file.  Note that in general, calling IUnknown::Release without first calling <b>IPropertyStorage::Commit</b> will discard any changes made; this workaround is specific to the image file property handler on Windows XP.  Also note that on later versions of Windows, this component functions properly (that is, calling <b>IPropertyStorage::Commit</b> persists changes and calling IUnknown::Release without calling <b>IPropertyStorage::Commit</b> discards them).

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readmultiple">IPropertyStorage::ReadMultiple</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a>
