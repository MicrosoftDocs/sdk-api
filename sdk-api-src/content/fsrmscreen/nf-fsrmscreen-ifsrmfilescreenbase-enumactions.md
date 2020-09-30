---
UID: NF:fsrmscreen.IFsrmFileScreenBase.EnumActions
title: IFsrmFileScreenBase::EnumActions (fsrmscreen.h)
description: Enumerates all the actions for the file screen object.
helpviewer_keywords: ["EnumActions","EnumActions method [File Server Resource Manager]","EnumActions method [File Server Resource Manager]","IFsrmFileScreenBase interface","IFsrmFileScreenBase interface [File Server Resource Manager]","EnumActions method","IFsrmFileScreenBase.EnumActions","IFsrmFileScreenBase::EnumActions","fs.ifsrmfilescreenbase_enumactions","fsrm.ifsrmfilescreenbase_enumactions","fsrmscreen/IFsrmFileScreenBase::EnumActions"]
old-location: fsrm\ifsrmfilescreenbase_enumactions.htm
tech.root: fsrm
ms.assetid: fbc22338-8271-407a-97c6-4a2329445979
ms.date: 12/05/2018
ms.keywords: EnumActions, EnumActions method [File Server Resource Manager], EnumActions method [File Server Resource Manager],IFsrmFileScreenBase interface, IFsrmFileScreenBase interface [File Server Resource Manager],EnumActions method, IFsrmFileScreenBase.EnumActions, IFsrmFileScreenBase::EnumActions, fs.ifsrmfilescreenbase_enumactions, fsrm.ifsrmfilescreenbase_enumactions, fsrmscreen/IFsrmFileScreenBase::EnumActions
req.header: fsrmscreen.h
req.include-header: FsrmScreen.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmScreen.idl
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
 - IFsrmFileScreenBase::EnumActions
 - fsrmscreen/IFsrmFileScreenBase::EnumActions
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
 - IFsrmFileScreenBase.EnumActions
---

# IFsrmFileScreenBase::EnumActions


## -description

Enumerates all the actions for the file screen object.

## -parameters

### -param actions [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> interface that contains a collection of actions that are defined for the object.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member for the <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a> interface. You can then use the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-get_actiontype">IFsrmAction::ActionType</a> property to determine the type of action.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenbase">IFsrmFileScreenBase</a>