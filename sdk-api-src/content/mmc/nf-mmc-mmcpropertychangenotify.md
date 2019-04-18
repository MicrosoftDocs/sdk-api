---
UID: NF:mmc.MMCPropertyChangeNotify
title: MMCPropertyChangeNotify function (mmc.h)
author: windows-sdk-content
description: Enables a snap-in property sheet to notify its IComponent or IComponentData interface that an item's properties have changed.
old-location: mmc\mmcpropertychangenotify.htm
tech.root: mmc
ms.assetid: f563a6dd-22e7-4839-bd44-1702ab3e17a3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MMCPropertyChangeNotify, MMCPropertyChangeNotify callback, MMCPropertyChangeNotify callback function [MMC], _slate_mmcpropertychangenotify, mmc.mmcpropertychangenotify, mmc/MMCPropertyChangeNotify
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
 - MMCPropertyChangeNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MMCPropertyChangeNotify function


## -description


The 
MMCPropertyChangeNotify function enables a snap-in property sheet to notify its 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> or 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> interface that an item's properties have changed.

Property sheets run in a different thread than their 
IComponent and 
IComponentData server; therefore, if <i>param</i> is a COM interface pointer, it must be marshaled. Asynchronously calling this function notifies the 
IComponent or the 
IComponentData associated with the property page whose properties have changed.


## -parameters




### -param lNotifyHandle [in]

A value that specifies the handle used to route the notification message to the appropriate 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> or 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>.


### -param param [in]

User-defined. Can be used freely.


## -returns



This callback function can return one of these values.




## -remarks



This is the handle passed to <a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a>.

A call to 
<i>MMCPropertyChangeNotify</i> causes an <a href="https://msdn.microsoft.com/4b1c6d78-23b1-4b5a-b913-8a7153471785">MMCN_PROPERTY_CHANGE</a> notification to be sent to the snap-in.

The <i>param</i> value that is passed to 
<i>MMCPropertyChangeNotify</i> is, in turn, forwarded to the snap-in as the <i>param</i> argument to MMCN_PROPERTY_CHANGE.




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/9beb0a0a-b3bf-46d0-b10c-0fc3ab25c18d">IExtendPropertySheet2</a>



<a href="https://msdn.microsoft.com/92802835-4324-4678-be9c-51dc9ca27576">MMCFreeNotifyHandle</a>
 

 

