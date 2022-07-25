---
UID: NE:wtypes.tagSTGC
title: STGC (wtypes.h)
description: Specify the conditions for performing the commit operation in the IStorage::Commit and IStream::Commit methods.
helpviewer_keywords: ["STGC","STGC enumeration [Structured Storage]","STGC_CONSOLIDATE","STGC_DANGEROUSLYCOMMITMERELYTODISKCACHE","STGC_DEFAULT","STGC_ONLYIFCURRENT","STGC_OVERWRITE","_stg_stgc","stg.stgc","wtypes/STGC","wtypes/STGC_CONSOLIDATE","wtypes/STGC_DANGEROUSLYCOMMITMERELYTODISKCACHE","wtypes/STGC_DEFAULT","wtypes/STGC_ONLYIFCURRENT","wtypes/STGC_OVERWRITE"]
old-location: stg\stgc.htm
tech.root: Stg
ms.assetid: f37260c0-d03d-4ead-a342-d2454ce8b1ac
ms.date: 12/05/2018
ms.keywords: STGC, STGC enumeration [Structured Storage], STGC_CONSOLIDATE, STGC_DANGEROUSLYCOMMITMERELYTODISKCACHE, STGC_DEFAULT, STGC_ONLYIFCURRENT, STGC_OVERWRITE, _stg_stgc, stg.stgc, wtypes/STGC, wtypes/STGC_CONSOLIDATE, wtypes/STGC_DANGEROUSLYCOMMITMERELYTODISKCACHE, wtypes/STGC_DEFAULT, wtypes/STGC_ONLYIFCURRENT, wtypes/STGC_OVERWRITE
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STGC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTGC
 - wtypes/tagSTGC
 - STGC
 - wtypes/STGC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WTypes.h
api_name:
 - STGC
---

# STGC enumeration


## -description

The 
<b>STGC</b> enumeration constants specify the conditions for performing the commit operation in the 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a> and 
<a href="/windows/desktop/api/objidl/nf-objidl-istream-commit">IStream::Commit</a> methods.

## -enum-fields

### -field STGC_DEFAULT:0

You can specify this condition with <b>STGC_CONSOLIDATE</b>, or some combination of the other three flags in this list of elements. Use this value to increase the readability of code.

### -field STGC_OVERWRITE:1

The commit operation can overwrite existing data to reduce overall space requirements. This value is not recommended for typical usage because it is not as robust as the default value. In this case, it is possible for the commit operation to fail after the old data is overwritten, but before the new data is completely committed. Then, neither the old version nor the new version of the storage object will be intact. 



						

You can use this value in the following cases:

<ul>
<li>The user is willing to risk losing the data.</li>
<li>The low-memory save sequence will be used to safely save the storage object to a smaller file.</li>
<li>A previous commit returned <b>STG_E_MEDIUMFULL</b>, but overwriting the existing data would provide enough space to commit changes to the storage object.</li>
</ul>
Be aware that the commit operation verifies that adequate space exists before any overwriting occurs. Thus, even with this value specified, if the commit operation fails due to space requirements, the old data is safe. It is possible, however, for data loss to occur with the <b>STGC_OVERWRITE</b> value specified if the commit operation fails for any reason other than lack of disk space.

### -field STGC_ONLYIFCURRENT:2

Prevents multiple users of a storage object from overwriting each other's changes. The commit operation occurs only if there have been no changes to the saved storage object because the user most recently opened it. Thus, the saved version of the storage object is the same version that the user has been editing. If other users have changed the storage object, the commit operation fails and returns the STG_E_NOTCURRENT value. To override this behavior, call the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a> or <a href="/windows/desktop/api/objidl/nf-objidl-istream-commit">IStream::Commit</a> method again using the <b>STGC_DEFAULT</b> value.

### -field STGC_DANGEROUSLYCOMMITMERELYTODISKCACHE:4

Commits the changes to a write-behind disk cache, but does not save the cache to the disk. In a write-behind disk cache, the operation that writes to disk actually writes to a disk cache, thus increasing performance. The cache is eventually written to the disk, but usually not until after the write operation has already returned. The performance increase comes at the expense of an increased risk of losing data if a problem occurs before the cache is saved and the data in the cache is lost. 




If you do not specify this value, then committing changes to root-level storage objects is robust even if a disk cache is used. The two-phase commit process ensures that data is stored on the disk and not just to the disk cache.

### -field STGC_CONSOLIDATE:8

Windows 2000 and Windows XP: Indicates that a storage should be consolidated after it is committed, resulting in a smaller file on disk. This flag is valid only on the outermost storage object that has been opened in transacted mode. It is not valid for streams. The <b>STGC_CONSOLIDATE</b> flag can be combined with any other STGC flags.

## -remarks

You can specify <b>STGC_DEFAULT</b> or some combination of <b>STGC_OVERWRITE</b>, <b>STGC_ONLYIFCURRENT</b>, and <b>STGC_DANGEROUSLYCOMMITMERELYTODISKCACHE</b> for normal commit operations. You can specify <b>STGC_CONSOLIDATE</b> with any other STGC flags.

Typically, use <b>STGC_ONLYIFCURRENT</b> to protect the storage object in cases where more than one user can edit the object simultaneously.

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>
