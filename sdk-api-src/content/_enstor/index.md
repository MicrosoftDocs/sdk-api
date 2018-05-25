---
UID: TP:enstor
ms.assetid: 233ef84c-dce9-3d93-bcda-5f4649228169
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Enhanced Storage



Overview of the Enhanced Storage technology.

To develop Enhanced Storage, you need these headers:

 * [ehstorapi.h](..\ehstorapi\index.md)
 * [ehstorextensions.h](..\ehstorextensions\index.md)

For the programming guide, see [Enhanced Storage](/previous-versions/windows/desktop/enstor).

## Structures

| Title   | Description   |
| ---- |:---- |
| [_ACT_AUTHORIZATION_STATE structure](..\ehstorapi\ns-ehstorapi-_act_authorization_state.md) | ACT_AUTHORIZATION_STATE structure contains data that describes the current authorization state of a Addressable Command Target (ACT). |
| [_ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION structure](..\ehstorextensions\ns-ehstorextensions-_enhanced_storage_password_silo_information.md) | ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION structure contains data that defines the capabilities and requirements of a password silo. |
| [_SILO_INFO structure](..\ehstorapi\ns-ehstorapi-_silo_info.md) | SILO_INFO structure contains information that identifies and describes the silo. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IEnhancedStorageACT interface](..\ehstorapi\nn-ehstorapi-ienhancedstorageact.md) | This interface to obtain information and perform operations for an 1667 Addressable Contact Target (ACT). |
| [IEnhancedStorageACT2 interface](..\ehstorapi\nn-ehstorapi-ienhancedstorageact2.md) | IEnhancedStorageACT2 interface is used to obtain information for a 1667 Addressable Contact Target (ACT). |
| [IEnhancedStorageSilo interface](..\ehstorapi\nn-ehstorapi-ienhancedstoragesilo.md) | IEnhancedStorageSilo interface is the point of access for an IEEE 1667 silo and is used to obtain information and perform operations at the silo level. |
| [IEnhancedStorageSiloAction interface](..\ehstorapi\nn-ehstorapi-ienhancedstoragesiloaction.md) | Use this interface as a point of access for actions involving IEEE 1667 silos. |
| [IEnumEnhancedStorageACT interface](..\ehstorapi\nn-ehstorapi-ienumenhancedstorageact.md) | Use this interface as the top level enumerator for all IEEE 1667 Addressable Contact Targets (ACT). |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IEnhancedStorageACT2::GetDeviceName](..\ehstorapi\nf-ehstorapi-ienhancedstorageact2-getdevicename.md) | IEnhancedStorageACT2 |
| [IEnhancedStorageACT2::IsDeviceRemovable](..\ehstorapi\nf-ehstorapi-ienhancedstorageact2-isdeviceremovable.md) | IEnhancedStorageACT2 |
| [IEnhancedStorageACT::Authorize](..\ehstorapi\nf-ehstorapi-ienhancedstorageact-authorize.md) | Associates the Addressable Command Target (ACT) with the Authorized state defined by ACT_AUTHORIZATION_STATE, and ensures the authentication of each individual silo according to the required sequence and logical combination necessary to authorize access to the ACT. |
| [IEnhancedStorageACT::GetAuthorizationState](..\ehstorapi\nf-ehstorapi-ienhancedstorageact-getauthorizationstate.md) | Returns the current authorization state of the ACT. |
| [IEnhancedStorageACT::GetMatchingVolume](..\ehstorapi\nf-ehstorapi-ienhancedstorageact-getmatchingvolume.md) | Returns the volume associated with the Addressable Command Target (ACT). |
| [IEnhancedStorageACT::GetSilos](..\ehstorapi\nf-ehstorapi-ienhancedstorageact-getsilos.md) | Returns an enumeration of all silos associated with the Addressable Command Target (ACT). |
| [IEnhancedStorageACT::GetUniqueIdentity](..\ehstorapi\nf-ehstorapi-ienhancedstorageact-getuniqueidentity.md) | Retrieves the unique identity of the Addressable Command Targer (ACT). |
| [IEnhancedStorageACT::Unauthorize](..\ehstorapi\nf-ehstorapi-ienhancedstorageact-unauthorize.md) | Associates the Addressable Command Target (ACT) with the Unauthorized state defined by ACT_AUTHORIZATION_STATE, and ensures the deauthentication of each individual silo according to the required sequence and logical combination necessary to restrict access to the ACT. |
| [IEnhancedStorageSilo::GetActions](..\ehstorapi\nf-ehstorapi-ienhancedstoragesilo-getactions.md) | Returns an enumeration of all actions available to the silo object. |
| [IEnhancedStorageSilo::GetDevicePath](..\ehstorapi\nf-ehstorapi-ienhancedstoragesilo-getdevicepath.md) | Retrieves the path to the silo device node. The returned string is suitable for passing to Windows System APIs such as CreateFile or SetupDiOpenDeviceInterface. |
| [IEnhancedStorageSilo::GetInfo](..\ehstorapi\nf-ehstorapi-ienhancedstoragesilo-getinfo.md) | Returns the descriptive information associated with the silo object. |
| [IEnhancedStorageSilo::GetPortableDevice](..\ehstorapi\nf-ehstorapi-ienhancedstoragesilo-getportabledevice.md) | Obtains an IPortableDevice pointer used to issue commands to the corresponding Enhanced Storage silo driver. |
| [IEnhancedStorageSilo::SendCommand](..\ehstorapi\nf-ehstorapi-ienhancedstoragesilo-sendcommand.md) | Sends a raw silo command to the silo object. This method is utilized to communicate with a silo which is not represented by a driver. |
| [IEnhancedStorageSiloAction::GetDescription](..\ehstorapi\nf-ehstorapi-ienhancedstoragesiloaction-getdescription.md) | Returns a descriptive string for the action specified by the IEnhancedStorageSiloAction object. |
| [IEnhancedStorageSiloAction::GetName](..\ehstorapi\nf-ehstorapi-ienhancedstoragesiloaction-getname.md) | Returns a string for the name of the action specified by the IEnhancedStorageSiloAction object. |
| [IEnhancedStorageSiloAction::Invoke](..\ehstorapi\nf-ehstorapi-ienhancedstoragesiloaction-invoke.md) | Performs the action specified by an IEnhancedStorageSiloAction object. |
| [IEnumEnhancedStorageACT::GetACTs](..\ehstorapi\nf-ehstorapi-ienumenhancedstorageact-getacts.md) | Returns an enumeration of all the Addressable Command Targets (ACT) currently connected to the system. If at least one ACT is present, the Enhanced Storage API allocates an array of 1 or more IEnumEnhancedStorageACT pointers. |
| [IEnumEnhancedStorageACT::GetMatchingACT](..\ehstorapi\nf-ehstorapi-ienumenhancedstorageact-getmatchingact.md) | Returns the Addressable Command Target (ACT) associated with the volume specified via the string supplied by the client. |
