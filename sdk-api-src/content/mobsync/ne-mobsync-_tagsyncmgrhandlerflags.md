---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _tagSYNCMGRHANDLERFLAGS enumeration


## -description


Used in the <a href="https://msdn.microsoft.com/8640796c-e5d0-48c8-b82b-7a153201e7de">SYNCMGRHANDLERINFO</a> structure as flags that apply to the current handler.


## -enum-fields




### -field SYNCMGRHANDLER_HASPROPERTIES

The current handler provides a property sheet dialog.


### -field SYNCMGRHANDLER_MAYESTABLISHCONNECTION


        May call back the <a href="https://msdn.microsoft.com/f7d1aff8-a77e-4067-9fc9-4adc69bfc0d1">ISyncMgrSynchronizeCallback::EstablishConnection</a> method. This value is ignored in <b>Windows Vista and later</b>.
      


### -field SYNCMGRHANDLER_ALWAYSLISTHANDLER


        Indicates Show Handler in Choice even if items are not shown. This value is ignored in <b>Windows Vista and later</b>.
      


### -field SYNCMGRHANDLER_HIDDEN

<b>Windows Vista and later</b>. Do not display handler or item.  This value is ignored by <b>Windows Vista</b>.
      


## -remarks




        Only the <b><b>SYNCMGRHANDLER_HASPROPERTIES</b></b> and <b><b>SYNCMGRHANDLER_HIDDEN</b></b> flags are recognized by Windows Vista. Although Windows Vista recognizes the <b><b>SYNCMGRHANDLER_HIDDEN</b></b> flag, it does not currently use it.  


          All flags are still valid for previous versions of Windows.
        




## -see-also




<a href="https://msdn.microsoft.com/8640796c-e5d0-48c8-b82b-7a153201e7de">SYNCMGRHANDLERINFO</a>
 

 

