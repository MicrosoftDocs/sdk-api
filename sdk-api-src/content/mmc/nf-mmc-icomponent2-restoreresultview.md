---
UID: NF:mmc.IComponent2.RestoreResultView
title: IComponent2::RestoreResultView (mmc.h)
description: The RestoreResultView method restores the result view. This method enables a snap-in to restore snap-in-specific details of a result view. For more information, see Restoring Result Views.
helpviewer_keywords: ["IComponent2 interface [MMC]","RestoreResultView method","IComponent2.RestoreResultView","IComponent2::RestoreResultView","RestoreResultView","RestoreResultView method [MMC]","RestoreResultView method [MMC]","IComponent2 interface","_slate_icomponent2_restoreresultview","mmc.icomponent2_restoreresultview","mmc/IComponent2::RestoreResultView"]
old-location: mmc\icomponent2_restoreresultview.htm
tech.root: mmc
ms.assetid: fe9a71c7-eaa6-4479-8337-0746a784a57f
ms.date: 12/05/2018
ms.keywords: IComponent2 interface [MMC],RestoreResultView method, IComponent2.RestoreResultView, IComponent2::RestoreResultView, RestoreResultView, RestoreResultView method [MMC], RestoreResultView method [MMC],IComponent2 interface, _slate_icomponent2_restoreresultview, mmc.icomponent2_restoreresultview, mmc/IComponent2::RestoreResultView
req.header: mmc.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComponent2::RestoreResultView
 - mmc/IComponent2::RestoreResultView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IComponent2.RestoreResultView
---

# IComponent2::RestoreResultView


## -description

The 
<b>RestoreResultView</b> method restores the result view. This method enables a snap-in to restore snap-in-specific details of a result view. For more information, see 
<a href="/previous-versions/windows/desktop/mmc/restoring-result-views">Restoring Result Views</a>.

This method supersedes the use of the 
<a href="/previous-versions/windows/desktop/mmc/mmcn-restore-view">MMCN_RESTORE_VIEW</a> notification.

## -parameters

### -param cookie [in]

A value that specifies the unique identifier whose result view will be restored.

### -param pResultViewType [in]

A pointer to the 
<a href="/windows/desktop/api/mmc/ns-mmc-result_view_type_info">RESULT_VIEW_TYPE_INFO</a> structure for the result view.

## -returns

If successful, the return value is S_OK. The snap-in can return S_FALSE to prevent MMC from restoring the view based on the information in *<i>pResultViewType</i>. Other return values indicate an error code.

## -remarks

The <b>pstrPersistableViewDescription</b> member of *<i>pResultViewType</i> specifies the name assigned to the result view.  To restore the result view identified by the <b>pstrPersistableViewDescription</b> member, the snap-in fills in the remaining members of *<i>pResultViewType</i>. The name of the result view is originally assigned during the snap-in's implementation of 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">IComponent2::GetResultViewType2</a>. MMC calls <b>IComponent2::RestoreResultView</b> so that the snap-in can restore internal view settings when the result view is revisited by the user.

When the user customizes the view, some of the settings (such as view options or view mode) are known by MMC, and some (such as <b>Oldest First</b> in the Event Viewer snap-in) are internal to the snap-in. Prior to MMC 2.0, there was no mechanism for MMC to communicate to the snap-in to restore the internal view settings. The <a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">IComponent2::GetResultViewType2</a> and <b>IComponent2::RestoreResultView</b> methods in MMC 2.0, however, provide the mechanism whereby internal view settings are restored. The snap-in persists internal view settings against the <b>pstrPersistableViewDescription</b> member of the <a href="/windows/desktop/api/mmc/ns-mmc-result_view_type_info">RESULT_VIEW_TYPE_INFO</a> structure. When MMC calls <b>IComponent2::RestoreResultView</b> to restore the result view, the snap-in uses the persisted settings to complete the view restoration.

The user revisits the result view by pressing the MMC <b>Back/Forward</b> buttons or loading a saved console file.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">IComponent2::GetResultViewType2</a>



<a href="/windows/desktop/api/mmc/ns-mmc-result_view_type_info">RESULT_VIEW_TYPE_INFO</a>



<a href="/previous-versions/windows/desktop/mmc/restoring-result-views">Restoring Result Views</a>