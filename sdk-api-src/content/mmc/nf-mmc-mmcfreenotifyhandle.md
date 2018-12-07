---
UID: NF:mmc.MMCFreeNotifyHandle
title: MMCFreeNotifyHandle function
author: windows-sdk-content
description: Called by a snap-in to free the handle to an MMCN_PROPERTY_CHANGE notification message sent to the snap-in by MMC in response to an MMCPropertyChangeNotify call made by a property sheet.
old-location: mmc\mmcfreenotifyhandle.htm
tech.root: mmc
ms.assetid: 92802835-4324-4678-be9c-51dc9ca27576
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MMCFreeNotifyHandle, MMCFreeNotifyHandle callback, MMCFreeNotifyHandle callback function [MMC], _slate_mmcfreenotifyhandle, mmc.mmcfreenotifyhandle, mmc/MMCFreeNotifyHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mmc.h
api_name:
 - MMCFreeNotifyHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MMCFreeNotifyHandle function


## -description


The 
MMCFreeNotifyHandle function is called by a snap-in to free the handle to an 
<a href="https://msdn.microsoft.com/4b1c6d78-23b1-4b5a-b913-8a7153471785">MMCN_PROPERTY_CHANGE</a> notification message sent to the snap-in by MMC in response to an 
<a href="https://msdn.microsoft.com/f563a6dd-22e7-4839-bd44-1702ab3e17a3">MMCPropertyChangeNotify</a> call made by a property sheet.


## -parameters




### -param lNotifyHandle [in]

A value that specifies a handle provided by the console during an 
<a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a> call.


## -returns



This callback function can return one of these values.




## -remarks



The handle to the notification is passed to the snap-in through a call to the 
<a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a> method. If the snap-in returns a success code (S_OK, S_FALSE) from this method, then the snap-in must call 
<i>MMCFreeNotifyHandle</i>. If the snap-in returns an error code, then MMC immediately frees the handle.

The snap-in can free the handle at any time, because MMC does not use the handle after it is given to the snap-in. The snap-in must only call 
<i>MMCFreeNotifyHandle</i> once and it must not use the handle in an 
<a href="https://msdn.microsoft.com/f563a6dd-22e7-4839-bd44-1702ab3e17a3">MMCPropertyChangeNotify</a> call after it is freed.

Be aware that the snap-in only must call 
<i>MMCFreeNotifyHandle</i> if its 
<a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a> method is called. MMC will not call <b>IExtendPropertySheet2::CreatePropertyPages</b> if the snap-in uses 
<a href="https://msdn.microsoft.com/e2115929-692e-4e59-bcdb-f37b02c53224">IPropertySheetCallback</a> to add property pages and then calls <a href="https://msdn.microsoft.com/f555dfd0-8af3-422f-a339-ab79daa89b45">IPropertySheetProvider::AddPrimaryPages</a> with a <b>NULL</b> first parameter. Calling 
AddPrimaryPages in this way informs MMC that the pages have already been added, so it is not required to call the snap-in's <b>IExtendPropertySheet2::CreatePropertyPages</b> method. For more information, see 
<a href="https://msdn.microsoft.com/d00e0e6d-3416-47c0-8d70-dcdacba220d0">Adding Wizard Pages: Implementation Details</a>.

The following list contains scenarios that illustrate situations in which the snap-in can call 
<i>MMCFreeNotifyHandle</i>:

<ul>
<li>In <a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a>, the snap-in does not add any property pages. If 
CreatePropertyPages does not return an error result, the snap-in can call 
MMCFreeNotifyHandle before returning. Otherwise, MMC will free the handle.</li>
<li>In <a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a>, the snap-in adds property pages, but does not pass the handle to the pages. Again, if 
CreatePropertyPages does not return an error result, the snap-in can call 
MMCFreeNotifyHandle before returning.</li>
<li>In <a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a>, the snap-in adds property pages and also passes the handle to the pages. However, the property pages do not call 
<a href="https://msdn.microsoft.com/f563a6dd-22e7-4839-bd44-1702ab3e17a3">MMCPropertyChangeNotify</a>. In this case, the snap-in can call 
<i>MMCFreeNotifyHandle</i> either in the destructor of the property pages or before returning (without an error result) from 
CreatePropertyPages.</li>
<li>In <a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a>, the snap-in adds property pages and also passes the handle to the pages. The property pages call 
<a href="https://msdn.microsoft.com/f563a6dd-22e7-4839-bd44-1702ab3e17a3">MMCPropertyChangeNotify</a>. In this case, the snap-in should call 
<i>MMCFreeNotifyHandle</i> in the destructor of the property pages. Be aware that calling 
<i>MMCFreeNotifyHandle</i> in the snap-in's <a href="https://msdn.microsoft.com/4b1c6d78-23b1-4b5a-b913-8a7153471785">MMCN_PROPERTY_CHANGE</a> notification handler is not recommended, because multiple pages may send notifications, or the same page could send multiple notifications (one each time the user clicks the <b>Apply</b> button).</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a>



<a href="https://msdn.microsoft.com/f563a6dd-22e7-4839-bd44-1702ab3e17a3">MMCPropertyChangeNotify</a>
 

 

