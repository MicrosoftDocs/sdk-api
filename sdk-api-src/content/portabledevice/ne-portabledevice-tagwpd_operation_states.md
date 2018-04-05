---
UID: NE:portabledevice.tagWPD_OPERATION_STATES
title: tagWPD_OPERATION_STATES
author: windows-driver-content
description: The WPD_OPERATION_STATES enumeration values describe the current state of an operation in progress.
old-location: wpdsdk\wpd_operation_states.htm
old-project: wpd_sdk
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_OPERATION_STATES, WPD_OPERATION_STATES enumeration [Windows Portable Devices SDK], WPD_OPERATION_STATE_ABORTED, WPD_OPERATION_STATE_CANCELLED, WPD_OPERATION_STATE_FINISHED, WPD_OPERATION_STATE_PAUSED, WPD_OPERATION_STATE_RUNNING, WPD_OPERATION_STATE_STARTED, WPD_OPERATION_STATE_UNSPECIFIED, portabledevice/WPD_OPERATION_STATES, portabledevice/WPD_OPERATION_STATE_ABORTED, portabledevice/WPD_OPERATION_STATE_CANCELLED, portabledevice/WPD_OPERATION_STATE_FINISHED, portabledevice/WPD_OPERATION_STATE_PAUSED, portabledevice/WPD_OPERATION_STATE_RUNNING, portabledevice/WPD_OPERATION_STATE_STARTED, portabledevice/WPD_OPERATION_STATE_UNSPECIFIED, tagWPD_OPERATION_STATES, wpdsdk.wpd_operation_states
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: portabledevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WPD_OPERATION_STATES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_OPERATION_STATES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_OPERATION_STATES enumeration


## -description



        The <b>WPD_OPERATION_STATES</b> enumeration values describe the current state of an operation in progress.
      


## -enum-fields




### -field WPD_OPERATION_STATE_UNSPECIFIED


            The current operation is in an unspecified state (not set) and unknown.
          


### -field WPD_OPERATION_STATE_STARTED


            The operation is started.
          


### -field WPD_OPERATION_STATE_RUNNING


            The operation is running.
          


### -field WPD_OPERATION_STATE_PAUSED


            The operation is paused.
          


### -field WPD_OPERATION_STATE_CANCELLED


            The operation is canceled.
          


### -field WPD_OPERATION_STATE_FINISHED


            The operation is finished.
          


### -field WPD_OPERATION_STATE_ABORTED


            The operation is aborted.
          


## -remarks




        These values are received in the application-defined callback (<a href="https://msdn.microsoft.com/1fb2d5d8-82b8-4c51-a086-bdcad33da190">IPortableDeviceEventCallback</a>).
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

