---
UID: NE:portabledevice.tagDELETE_OBJECT_OPTIONS
title: tagDELETE_OBJECT_OPTIONS
author: windows-driver-content
description: The DELETE_OBJECT_OPTIONS enumeration type describes options that are supported by a device when deleting an object.
old-location: wpdsdk\delete_object_options.htm
old-project: wpd_sdk
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: DELETE_OBJECT_OPTIONS, DELETE_OBJECT_OPTIONS enumeration [Windows Portable Devices SDK], PORTABLE_DEVICE_DELETE_NO_RECURSION, PORTABLE_DEVICE_DELETE_WITH_RECURSION, enumeration [Windows Portable Devices SDK], portabledevice/DELETE_OBJECT_OPTIONS, portabledevice/PORTABLE_DEVICE_DELETE_NO_RECURSION, portabledevice/PORTABLE_DEVICE_DELETE_WITH_RECURSION, tagDELETE_OBJECT_OPTIONS, wpdsdk.delete_object_options
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
req.typenames: DELETE_OBJECT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	DELETE_OBJECT_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagDELETE_OBJECT_OPTIONS enumeration


## -description



        The <b>DELETE_OBJECT_OPTIONS</b> enumeration type describes options that are supported by a device when deleting an object.
      


## -enum-fields




### -field PORTABLE_DEVICE_DELETE_NO_RECURSION


            Delete the object only and fail if it has children.
          


### -field PORTABLE_DEVICE_DELETE_WITH_RECURSION


            Delete the object and all its children.
          


## -remarks




        The application can retrieve the deletion options that the device supports by calling <a href="https://msdn.microsoft.com/d222968f-3ca7-4a4d-bdc6-89a6ca98c7b0">IPortableDeviceCapabilities::GetCommandOptions</a> for the <b>WPD_COMMAND_OBJECT_MANAGEMENT_DELETE_OBJECTS</b> command. It should examine the <b>WPD_OPTION_OBJECT_MANAGEMENT_RECURSIVE_DELETE_SUPPORTED</b> option value that this method returns in an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597598">IPortableDeviceValuesCollection</a> object.
      




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597672">Structures and Enumeration Types</a>
 

 

