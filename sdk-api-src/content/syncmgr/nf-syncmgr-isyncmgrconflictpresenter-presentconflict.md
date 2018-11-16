---
UID: NF:syncmgr.ISyncMgrConflictPresenter.PresentConflict
title: ISyncMgrConflictPresenter::PresentConflict
author: windows-sdk-content
description: Presents the conflict to the user.
old-location: shell\ISyncMgrConflictPresenter_PresentConflict.htm
tech.root: shell
ms.assetid: 632c0e9c-facd-422e-9467-005c44adc175
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISyncMgrConflictPresenter interface [Windows Shell],PresentConflict method, ISyncMgrConflictPresenter.PresentConflict, ISyncMgrConflictPresenter::PresentConflict, PresentConflict, PresentConflict method [Windows Shell], PresentConflict method [Windows Shell],ISyncMgrConflictPresenter interface, _shell_ISyncMgrConflictPresenter_PresentConflict, shell.ISyncMgrConflictPresenter_PresentConflict, syncmgr/ISyncMgrConflictPresenter::PresentConflict
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrConflictPresenter.PresentConflict
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- syncmgr.h
: 
- ISyncMgrConflictPresenter.PresentConflict
: 
---

# ISyncMgrConflictPresenter::PresentConflict


## -description


Presents the conflict to the user.


## -parameters




### -param pConflict [in]

Type: <b><a href="https://msdn.microsoft.com/a5806a83-b470-4617-961d-b768160afc48">ISyncMgrConflict</a>*</b>

Specifies the conflict. See <a href="https://msdn.microsoft.com/a5806a83-b470-4617-961d-b768160afc48">ISyncMgrConflict</a>.


### -param pResolveInfo [in]

Type: <b><a href="https://msdn.microsoft.com/c47d533f-7307-4db3-a025-961f3419203e">ISyncMgrConflictResolveInfo</a>*</b>


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



