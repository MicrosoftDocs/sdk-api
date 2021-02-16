---
UID: NF:fsrm.IFsrmCommittableCollection.Commit
title: IFsrmCommittableCollection::Commit (fsrm.h)
description: Commits all the objects of the collection and returns the commit results for each object.
helpviewer_keywords: ["Commit","Commit method [File Server Resource Manager]","Commit method [File Server Resource Manager]","IFsrmCommittableCollection interface","IFsrmCommittableCollection interface [File Server Resource Manager]","Commit method","IFsrmCommittableCollection.Commit","IFsrmCommittableCollection::Commit","fs.ifsrmcommitablecollection_commit","fs.ifsrmcommittablecollection_commit","fsrm.ifsrmcommittablecollection_commit","fsrm/IFsrmCommittableCollection::Commit"]
old-location: fsrm\ifsrmcommittablecollection_commit.htm
tech.root: fsrm
ms.assetid: 844cb2a5-8526-434b-af22-b1bf856ed6af
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [File Server Resource Manager], Commit method [File Server Resource Manager],IFsrmCommittableCollection interface, IFsrmCommittableCollection interface [File Server Resource Manager],Commit method, IFsrmCommittableCollection.Commit, IFsrmCommittableCollection::Commit, fs.ifsrmcommitablecollection_commit, fs.ifsrmcommittablecollection_commit, fsrm.ifsrmcommittablecollection_commit, fsrm/IFsrmCommittableCollection::Commit
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmCommittableCollection::Commit
 - fsrm/IFsrmCommittableCollection::Commit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmCommittableCollection.Commit
---

# IFsrmCommittableCollection::Commit


## -description

Commits all the objects of the collection and returns the commit results for each 
    object.

## -parameters

### -param options [in]

One or more options to use when committing the collection of objects. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmcommitoptions">FsrmCommitOptions</a> enumeration.

### -param results [out]

A collection of <b>HRESULT</b> values that correspond directly to the objects in the 
       collection. The <b>HRESULT</b> value indicates the success or failure of committing the 
       object.

If the method returns <b>FSRM_S_PARTIAL_BATCH</b> or 
       <b>FSRM_E_FAIL_BATCH</b>, check the results.

## -returns

The method returns the following return values.

## -remarks

Committing objects in a batch operation provides better performance than committing each object in the 
    collection individually (for example, calling the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmFileScreen::Commit</a> method).

Note that the state of the objects in the collection must be the same. For example, the collection must 
    contain all new objects, objects marked for deletion, or modified objects. The modified category covers objects 
    are not new or marked for deletion—it does not necessarily mean that they've been 
    modified.

A collection of imported objects would be considered a collection of modified objects. If you marked one or 
    more of the imported objects for deletion (called the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-delete">Delete</a> method on the object), you would first have to 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmmutablecollection-remove">remove</a> those objects from the collection before 
    committing the rest.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a>