---
UID: NF:mmc.IPropertySheetProvider.AddPrimaryPages
title: IPropertySheetProvider::AddPrimaryPages (mmc.h)
description: The IPropertySheetProvider::AddPrimaryPages method collects the pages from the primary snap-in.
helpviewer_keywords: ["AddPrimaryPages","AddPrimaryPages method [MMC]","AddPrimaryPages method [MMC]","IPropertySheetProvider interface","IPropertySheetProvider interface [MMC]","AddPrimaryPages method","IPropertySheetProvider.AddPrimaryPages","IPropertySheetProvider::AddPrimaryPages","_slate_ipropertysheetprovider_addprimarypages","mmc.ipropertysheetprovider_addprimarypages","mmc/IPropertySheetProvider::AddPrimaryPages"]
old-location: mmc\ipropertysheetprovider_addprimarypages.htm
tech.root: mmc
ms.assetid: f555dfd0-8af3-422f-a339-ab79daa89b45
ms.date: 12/05/2018
ms.keywords: AddPrimaryPages, AddPrimaryPages method [MMC], AddPrimaryPages method [MMC],IPropertySheetProvider interface, IPropertySheetProvider interface [MMC],AddPrimaryPages method, IPropertySheetProvider.AddPrimaryPages, IPropertySheetProvider::AddPrimaryPages, _slate_ipropertysheetprovider_addprimarypages, mmc.ipropertysheetprovider_addprimarypages, mmc/IPropertySheetProvider::AddPrimaryPages
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
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertySheetProvider::AddPrimaryPages
 - mmc/IPropertySheetProvider::AddPrimaryPages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IPropertySheetProvider.AddPrimaryPages
---

# IPropertySheetProvider::AddPrimaryPages


## -description

The <b>IPropertySheetProvider::AddPrimaryPages</b> method collects the pages from the primary snap-in.

## -parameters

### -param lpUnknown [in]

A pointer to snap-in interface that will be queried for the <b>IExtendPropertySheet</b> interface. If <i>bCreateHandle</i> is set to <b>TRUE</b>, this should also be a pointer to the snap-in's 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> or 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> interface that will be queried for <b>IExtendPropertySheet</b>. Be aware that this value can be <b>NULL</b>. See Remarks for details.

### -param bCreateHandle [in]

A value that specifies whether to create a console-provided notification handle that is used to route the <a href="/previous-versions/windows/desktop/mmc/mmcn-property-change">MMCN_PROPERTY_CHANGE</a> notification to the appropriate 
<b>IComponent</b> or 
<b>IComponentData</b> interface during calls to 
<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertychangenotify">MMCPropertyChangeNotify</a>. The notification handle is passed back to the snap-in during calls to the snap-in's implementation of the 
<a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a> method.

If <i>bCreateHandle</i> is set to <b>TRUE</b>, the <i>lpUnknown</i> parameter should be a pointer to the 
<b>IComponent</b> or 
<b>IComponentData</b> that receives the <a href="/previous-versions/windows/desktop/mmc/mmcn-property-change">MMCN_PROPERTY_CHANGE</a> notification.

### -param hNotifyWindow [in]

Reserved for future use. This value should be <b>NULL</b>.

### -param bScopePane [in]

Set to <b>TRUE</b> if the item is in the scope pane. Set to <b>FALSE</b> if it is in the result pane.

## -returns

This method can return one of these values.

## -remarks

The snap-in might not add any pages during this method call. If this is the case, extension pages should not be added.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetprovider">IPropertySheetProvider</a>



<a href="/previous-versions/windows/desktop/mmc/using-ipropertysheetprovider-directly">Using IPropertySheetProvider Directly</a>