---
UID: NE:devquerydef._DEV_OBJECT_TYPE
tech.root: devinst
title: DEV_OBJECT_TYPE
ms.date: 10/30/2024
targetos: Windows
description: Specifies the type of a DEV_OBJECT.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: devquerydef.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - devquerydef.h
api_name:
 - _DEV_OBJECT_TYPE
 - PDEV_OBJECT_TYPE
 - DEV_OBJECT_TYPE
f1_keywords:
 - _DEV_OBJECT_TYPE
 - devquerydef/_DEV_OBJECT_TYPE
 - PDEV_OBJECT_TYPE
 - devquerydef/PDEV_OBJECT_TYPE
 - DEV_OBJECT_TYPE
 - devquerydef/DEV_OBJECT_TYPE
dev_langs:
 - c++
helpviewer_keywords:
 - _DEV_OBJECT_TYPE
---

## -description

Specifies the type of a [DEV_OBJECT](ns-devquerydef-dev_object.md).

## -enum-fields

### -field DevObjectTypeUnknown

Not a valid object type.

### -field DevObjectTypeDeviceInterface

The object represents a device interface. These are exposed by device drivers to enable an app to talk to the device, typically using device IOCTLs (input output controls). For more information on device interfaces, see [Using a device interface](/windows-hardware/drivers/install/using-a-device-interface). For more information on IOCTLs, see [Introduction to I/O Control Codes](/windows-hardware/drivers/kernel/introduction-to-i-o-control-codes)

### -field DevObjectTypeDeviceContainer

The object represents a device container, which describe a collection of device objects that exist in the same physical device. For more information, see [Container ID](/windows-hardware/drivers/install/container-ids).

### -field DevObjectTypeDevice

The object represents a device. This could also be referred to as a devnode. These devices are objects that represent a piece of the device functionality and optionally have drivers loaded on them. For more information, see [Device instance ID](/windows-hardware/drivers/install/device-instance-ids).

### -field DevObjectTypeDeviceInterfaceClass

The object represents a device interface class. Every *DevObjectTypeDeviceInterface* object belongs to a certain device interface class. This is similar to a contract definition. For more information, see [Overview of device interface classes](/windows-hardware/drivers/install/overview-of-device-interface-classes).

### -field DevObjectTypeAEP

The object represents a device association endpoint (AEP). AEPs usually represent a device discovered over a wireless or network protocol.

### -field DevObjectTypeAEPContainer

The object represents an AEP container. This object represents a single physical device that might have more than one AEP objects associated with it. For example, if a television supports two different network protocols, the container would be the television. It would also have two AEP objects, one to represent each protocol.

### -field DevObjectTypeDeviceInstallerClass

The object represents a device setup class. For more information, see [Overview of device setup classes](/windows-hardware/drivers/install/overview-of-device-setup-classes).

### -field DevObjectTypeDeviceInterfaceDisplay

The object represents a device interface in the same way as a *DevObjectTypeDeviceInterface* object, but this object has some additional properties added to it that are taken from the device container the device interface is part of.

### -field DevObjectTypeDeviceContainerDisplay

The object is similar to a *DevObjectTypeDeviceContainer* object, but with some extra properties associated with the object.

### -field DevObjectTypeAEPService

The object represents an AEP Service. The object represents a functional service contract exposed by the device. Not all protocols support AEP services. An AEP service can have a single parent AEP and AEP container object.

### -field DevObjectTypeDevicePanel

The  object represents a single physical face of a device enclosure.

### -field DevObjectTypeAEPProtocol

The object represents a protocol through which association endpoints (AEPs) can be discovered. You can scope an association endpoint discovery to specific protocols by using the protocol ID. For example, a filter can scope discovery to Bluetooth LE or Bluetooth Classic.

## -remarks

## -see-also

