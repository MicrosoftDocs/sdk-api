---
UID: NF:mmc.MMCFreeNotifyHandle
title: MMCFreeNotifyHandle function (mmc.h)
description: Called by a snap-in to free the handle to an MMCN_PROPERTY_CHANGE notification message sent to the snap-in by MMC in response to an MMCPropertyChangeNotify call made by a property sheet.
helpviewer_keywords: ["MMCFreeNotifyHandle","MMCFreeNotifyHandle callback","MMCFreeNotifyHandle callback function [MMC]","_slate_mmcfreenotifyhandle","mmc.mmcfreenotifyhandle","mmc/MMCFreeNotifyHandle"]
old-location: mmc\mmcfreenotifyhandle.htm
tech.root: mmc
ms.assetid: 92802835-4324-4678-be9c-51dc9ca27576
ms.date: 12/05/2018
ms.keywords: MMCFreeNotifyHandle, MMCFreeNotifyHandle callback, MMCFreeNotifyHandle callback function [MMC], _slate_mmcfreenotifyhandle, mmc.mmcfreenotifyhandle, mmc/MMCFreeNotifyHandle
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
 - MMCFreeNotifyHandle
 - mmc/MMCFreeNotifyHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mmc.h
api_name:
 - MMCFreeNotifyHandle
---

# MMCFreeNotifyHandle function


## -description

The 
MMCFreeNotifyHandle function is called by a snap-in to free the handle to an 
<a href="/previous-versions/windows/desktop/mmc/mmcn-property-change">MMCN_PROPERTY_CHANGE</a> notification message sent to the snap-in by MMC in response to an 
<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertychangenotify">MMCPropertyChangeNotify</a> call made by a property sheet.

## -parameters

### -param lNotifyHandle [in]

A value that specifies a handle provided by the console during an 
<a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a> call.

## -returns

This callback function can return one of these values.

## -remarks

The handle to the notification is passed to the snap-in through a call to the 
<a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a> method. If the snap-in returns a success code (S_OK, S_FALSE) from this method, then the snap-in must call 
<i>MMCFreeNotifyHandle</i>. If the snap-in returns an error code, then MMC immediately frees the handle.

The snap-in can free the handle at any time, because MMC does not use the handle after it is given to the snap-in. The snap-in must only call 
<i>MMCFreeNotifyHandle</i> once and it must not use the handle in an 
<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertychangenotify">MMCPropertyChangeNotify</a> call after it is freed.

Be aware that the snap-in only must call 
<i>MMCFreeNotifyHandle</i> if its 
<a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a> method is called. MMC will not call <b>IExtendPropertySheet2::CreatePropertyPages</b> if the snap-in uses 
<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetcallback">IPropertySheetCallback</a> to add property pages and then calls <a href="/windows/desktop/api/mmc/nf-mmc-ipropertysheetprovider-addprimarypages">IPropertySheetProvider::AddPrimaryPages</a> with a <b>NULL</b> first parameter. Calling 
AddPrimaryPages in this way informs MMC that the pages have already been added, so it is not required to call the snap-in's <b>IExtendPropertySheet2::CreatePropertyPages</b> method. For more information, see 
<a href="/previous-versions/windows/desktop/mmc/adding-wizard-pages-implementation-details">Adding Wizard Pages: Implementation Details</a>.

The following list contains scenarios that illustrate situations in which the snap-in can call 
<i>MMCFreeNotifyHandle</i>:

<ul>
<li>In <a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a>, the snap-in does not add any property pages. If 
CreatePropertyPages does not return an error result, the snap-in can call 
MMCFreeNotifyHandle before returning. Otherwise, MMC will free the handle.</li>
<li>In <a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a>, the snap-in adds property pages, but does not pass the handle to the pages. Again, if 
CreatePropertyPages does not return an error result, the snap-in can call 
MMCFreeNotifyHandle before returning.</li>
<li>In <a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a>, the snap-in adds property pages and also passes the handle to the pages. However, the property pages do not call 
<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertychangenotify">MMCPropertyChangeNotify</a>. In this case, the snap-in can call 
<i>MMCFreeNotifyHandle</i> either in the destructor of the property pages or before returning (without an error result) from 
CreatePropertyPages.</li>
<li>In <a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a>, the snap-in adds property pages and also passes the handle to the pages. The property pages call 
<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertychangenotify">MMCPropertyChangeNotify</a>. In this case, the snap-in should call 
<i>MMCFreeNotifyHandle</i> in the destructor of the property pages. Be aware that calling 
<i>MMCFreeNotifyHandle</i> in the snap-in's <a href="/previous-versions/windows/desktop/mmc/mmcn-property-change">MMCN_PROPERTY_CHANGE</a> notification handler is not recommended, because multiple pages may send notifications, or the same page could send multiple notifications (one each time the user clicks the <b>Apply</b> button).</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)">IExtendPropertySheet2::CreatePropertyPages</a>



<a href="/windows/desktop/api/mmc/nf-mmc-mmcpropertychangenotify">MMCPropertyChangeNotify</a>