---
UID: NF:cscobj.IOfflineFilesConnectionInfo.TransitionOnline
title: IOfflineFilesConnectionInfo::TransitionOnline (cscobj.h)
description: Transitions an item online if possible.
helpviewer_keywords: ["IOfflineFilesConnectionInfo interface [Offline Files]","TransitionOnline method","IOfflineFilesConnectionInfo.TransitionOnline","IOfflineFilesConnectionInfo::TransitionOnline","OFFLINEFILES_TRANSITION_FLAG_CONSOLE","OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE","TransitionOnline","TransitionOnline method [Offline Files]","TransitionOnline method [Offline Files]","IOfflineFilesConnectionInfo interface","cscobj/IOfflineFilesConnectionInfo::TransitionOnline","of.iofflinefilesconnectioninfo_transitiononline"]
old-location: of\iofflinefilesconnectioninfo_transitiononline.htm
tech.root: of
ms.assetid: b8cac664-598d-43fd-a77e-e8406c197afc
ms.date: 12/05/2018
ms.keywords: IOfflineFilesConnectionInfo interface [Offline Files],TransitionOnline method, IOfflineFilesConnectionInfo.TransitionOnline, IOfflineFilesConnectionInfo::TransitionOnline, OFFLINEFILES_TRANSITION_FLAG_CONSOLE, OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE, TransitionOnline, TransitionOnline method [Offline Files], TransitionOnline method [Offline Files],IOfflineFilesConnectionInfo interface, cscobj/IOfflineFilesConnectionInfo::TransitionOnline, of.iofflinefilesconnectioninfo_transitiononline
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesConnectionInfo::TransitionOnline
 - cscobj/IOfflineFilesConnectionInfo::TransitionOnline
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesConnectionInfo.TransitionOnline
---

# IOfflineFilesConnectionInfo::TransitionOnline


## -description

Transitions an item online if possible.

## -parameters

### -param hwndParent [in]

Provides a parent window handle used for any interactive user interface elements such as credential request dialogs.  This parameter may be <b>NULL</b>.  This parameter is ignored if the OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE flag is not specified in the <i>dwFlags</i> parameter.

### -param dwFlags [in]

One or more of the following flag values:



#### OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE (0x00000001)

Set this flag if the operation is allowed to display user interface elements as necessary.  An example is the system's credential-request dialog.  If this flag is set, the value in hwndParent is used as the parent for any user interface elements displayed.



#### OFFLINEFILES_TRANSITION_FLAG_CONSOLE (0x00000002)

This flag is ignored if the OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE flag is not set.  If the OFFLINEFILES_TRANSITION_FLAG_INTERACTIVE flag is set, this flag indicates that any UI produced should be directed to the console window associated with the process invoking the operation.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

Note that the entire scope of the item is transitioned online, not just the item.  An item's scope is defined as the closest ancestor shared folder of the item.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesconnectioninfo">IOfflineFilesConnectionInfo</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-transitionoffline">IOfflineFilesConnectionInfo::TransitionOffline</a>