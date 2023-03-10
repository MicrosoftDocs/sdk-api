---
UID: NF:mmc.IComponent2.GetResultViewType2
title: IComponent2::GetResultViewType2 (mmc.h)
description: The GetResultViewType2 method retrieves the result view type. This method supersedes the IComponent::GetResultViewType method.
helpviewer_keywords: ["GetResultViewType2","GetResultViewType2 method [MMC]","GetResultViewType2 method [MMC]","IComponent2 interface","IComponent2 interface [MMC]","GetResultViewType2 method","IComponent2.GetResultViewType2","IComponent2::GetResultViewType2","_slate_icomponent2_getresultviewtype2","mmc.icomponent2_getresultviewtype2","mmc/IComponent2::GetResultViewType2"]
old-location: mmc\icomponent2_getresultviewtype2.htm
tech.root: mmc
ms.assetid: 687ddb0a-6e10-4553-9885-fd85bf8dd6ff
ms.date: 12/05/2018
ms.keywords: GetResultViewType2, GetResultViewType2 method [MMC], GetResultViewType2 method [MMC],IComponent2 interface, IComponent2 interface [MMC],GetResultViewType2 method, IComponent2.GetResultViewType2, IComponent2::GetResultViewType2, _slate_icomponent2_getresultviewtype2, mmc.icomponent2_getresultviewtype2, mmc/IComponent2::GetResultViewType2
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
 - IComponent2::GetResultViewType2
 - mmc/IComponent2::GetResultViewType2
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
 - IComponent2.GetResultViewType2
---

# IComponent2::GetResultViewType2


## -description

The 
<b>GetResultViewType2</b> method retrieves the result view type. This method supersedes the 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a> method.

## -parameters

### -param cookie [in]

A value that specifies the snapin-provided unique identifier for the scope item. For more details about cookies in MMC, see <a href="/previous-versions/windows/desktop/mmc/cookies">Cookies</a>.

### -param pResultViewType [in, out]

A pointer to the 
<a href="/windows/desktop/api/mmc/ns-mmc-result_view_type_info">RESULT_VIEW_TYPE_INFO</a> structure for the result view. If your snap-in implements 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent2">IComponent2</a>, the <b>pstrPersistableViewDescription</b> member of the <b>RESULT_VIEW_TYPE_INFO</b> structure must contain a valid view description string; otherwise, MMC will not initialize your snap-in. The <b>pstrPersistableViewDescription</b> member must be allocated by 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. The snap-in must not free <b>pstrPersistableViewDescription</b>, as it will be freed by MMC.

## -returns

If successful, the return value is S_OK. Other return values indicate an error code.

## -remarks

During result view creation, MMC calls the snap-in's <b>IComponent2::GetResultViewType2</b> method. When the user revisits the result view named by the <b>pstrPersistableViewDescription</b> member of *<i>pResultViewType</i>, MMC will call the snap-in's 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-restoreresultview">IComponent2::RestoreResultView</a> method, at which time the snap-in can provide snap-in-specific details (if any) for the restored result view. The user revisits the result view by means of the MMC <b>Back/Forward</b> buttons or the loading of a saved console file. For more information about the use of the <b>IComponent2::GetResultViewType2</b> and <b>IComponent2::RestoreResultView</b> methods, see 
<a href="/previous-versions/windows/desktop/mmc/restoring-result-views">Restoring Result Views</a>.

If the snap-in is implementing an OCX (ActiveX control) view, then the snap-in creates the OCX and provides MMC with the OCX 
<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer in the <a href="/windows/desktop/api/mmc/ns-mmc-result_view_type_info">RESULT_VIEW_TYPE_INFO</a> structure (specifically, the structure's <b>pUnkControl</b> member). The snap-in has control over the OCX creation, so the snap-in can address licensing or security issues as required. During the call to 
<b>GetResultViewType2</b>, the snap-in can also initialize the OCX (the snap-in will not receive a <a href="/previous-versions/windows/desktop/mmc/mmcn-initocx">MMCN_INITOCX</a> notification).

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-restoreresultview">IComponent2::RestoreResultView</a>



<a href="/windows/desktop/api/mmc/ns-mmc-result_view_type_info">RESULT_VIEW_TYPE_INFO</a>



<a href="/previous-versions/windows/desktop/mmc/restoring-result-views">Restoring Result Views</a>