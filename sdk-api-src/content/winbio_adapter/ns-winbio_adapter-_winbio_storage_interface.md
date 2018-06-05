---
UID: NS:winbio_adapter._WINBIO_STORAGE_INTERFACE
title: "_WINBIO_STORAGE_INTERFACE"
author: windows-sdk-content
description: Contains pointers to your custom storage adapter functions.
old-location: secbiomet\winbio_storage_interface.htm
old-project: SecBioMet
ms.assetid: 1cc7ce07-66df-43d9-9db2-50558a0f5f47
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: "*PWINBIO_STORAGE_INTERFACE, PWINBIO_STORAGE_INTERFACE, PWINBIO_STORAGE_INTERFACE structure pointer [Windows Biometric Framework API], WINBIO_STORAGE_INTERFACE, WINBIO_STORAGE_INTERFACE structure [Windows Biometric Framework API], _WINBIO_STORAGE_INTERFACE, secbiomet.winbio_storage_interface, winbio_adapter/PWINBIO_STORAGE_INTERFACE, winbio_adapter/WINBIO_STORAGE_INTERFACE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winbio_adapter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: "*PWINBIO_STORAGE_INTERFACE, WINBIO_STORAGE_INTERFACE"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_adapter.h
api_name:
-	WINBIO_STORAGE_INTERFACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_STORAGE_INTERFACE structure


## -description


The <b>WINBIO_STORAGE_INTERFACE</b> structure contains pointers to your custom storage adapter functions. The Windows Biometric Framework uses this structure to locate the functions.


## -struct-fields




### -field Version

Version number of this structure.

<b>Windows 10:  </b>The version number must be <b>WINBIO_STORAGE_INTERFACE_VERSION_3</b>.

<b>Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:  </b>The version number must be <b>WINBIO_STORAGE_INTERFACE_VERSION_2</b>.

<b>Windows Server 2008 R2 and Windows 7:  </b>The version number must be <b>WINBIO_STORAGE_INTERFACE_VERSION_1</b>.


### -field Type

The type of adapter. This must be <b>WINBIO_ADAPTER_TYPE_STORAGE</b>.


### -field Size

The size, in bytes, of this structure. Set this value to the size of the <b>WINBIO_STORAGE_INTERFACE</b> structure. 


### -field AdapterId

A GUID that uniquely identifies the storage adapter. You must generate this value.


### -field Attach

A pointer to your implementation of the <a href="https://msdn.microsoft.com/6abded6b-12e0-4cc6-a011-0b18e8ea747b">StorageAdapterAttach</a> function.


### -field Detach

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/cebf03d3-e393-437a-81f7-579fea95aa9c">StorageAdapterDetach</a> function.


### -field ClearContext

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/d7022363-01e9-4675-9bd0-e9369d237c3c">StorageAdapterClearContext</a> function.


### -field CreateDatabase

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/7b9e034e-51d4-4209-9092-14e21e9fff3c">StorageAdapterCreateDatabase</a> function.


### -field EraseDatabase

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/c1fc2f3f-034b-4546-aeee-1d1a38695793">StorageAdapterEraseDatabase</a> function.


### -field OpenDatabase

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/4f3dfa67-5020-461a-b3d1-33c948129bdf">StorageAdapterOpenDatabase</a> function.


### -field CloseDatabase

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/ddb8d0b8-e975-4ee2-bb8c-423b1304c467">StorageAdapterCloseDatabase</a> function.


### -field GetDataFormat

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/e5bf31aa-59d7-410a-bb11-fe4af36fa409">StorageAdapterGetDataFormat</a> function.


### -field GetDatabaseSize

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/98e26b32-3e2a-40d9-8463-9bd7e93c636b">StorageAdapterGetDatabaseSize</a> function.


### -field AddRecord

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/889664e2-00e8-49b4-9754-4ca72dd44bbd">StorageAdapterAddRecord</a> function.


### -field DeleteRecord

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/f1939410-1c1e-42e4-98d6-d8866d313ca1">StorageAdapterDeleteRecord</a> function.


### -field QueryBySubject

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/b2c93122-fae1-44ad-97d4-f90115194a31">StorageAdapterQueryBySubject</a> function.


### -field QueryByContent

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/773aacd1-a34a-4c5a-b615-2a5485f13ca1">StorageAdapterQueryByContent</a> function.


### -field GetRecordCount

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/dc7891c3-33f7-498c-acb1-4687909debb7">StorageAdapterGetRecordCount</a> function.


### -field FirstRecord

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/736688c3-2c2c-4244-9f49-98ad0fe2d141">StorageAdapterFirstRecord</a> function.


### -field NextRecord

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/e0025167-0778-474e-baca-ffc767822893">StorageAdapterNextRecord</a> function.


### -field GetCurrentRecord

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/a06550da-c6ea-44e5-b54f-8005bcbc0364">StorageAdapterGetCurrentRecord</a> function.


### -field ControlUnit

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/98981278-9d30-4e7d-a9b6-d0427ed8b385">StorageAdapterControlUnit</a> function.


### -field ControlUnitPrivileged

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/42e33817-df5f-4598-bc6a-94e49ce5fca4">StorageAdapterControlUnitPrivileged</a> function.


### -field NotifyPowerChange

A pointer to your implementation of the <a href="https://msdn.microsoft.com/22c2ce7b-6e30-40e1-bbe8-f0e479ddcc77">StorageAdapterNotifyPowerChange</a> function. This member is supported starting in Windows 8.


### -field PipelineInit

A pointer to your implementation of the <a href="https://msdn.microsoft.com/F969AC5A-6760-4904-A04E-F2FEF4290F7A">StorageAdapterPipelineInit</a> function. This member is supported starting in Windows 10.


### -field PipelineCleanup

A pointer to your implementation of the <a href="https://msdn.microsoft.com/4F75BCE0-173F-48F3-B4DD-A6AE1AFD4EA5">StorageAdapterPipelineCleanup</a> function. This member is supported starting in Windows 10.


### -field Activate

A pointer to your implementation of the <a href="https://msdn.microsoft.com/2E9B5191-94F2-4954-BE3A-78803ABBAD07">StorageAdapterActivate</a> function. This member is supported starting in Windows 10.


### -field Deactivate

A pointer to your implementation of the <a href="https://msdn.microsoft.com/95AAEE98-2DA6-4A2C-BF0C-DBE193346FE1">StorageAdapterDeactivate</a> function. This member is supported starting in Windows 10.


### -field QueryExtendedInfo

A pointer to your implementation of the <a href="https://msdn.microsoft.com/BCA55006-73F4-4845-84B3-34A6255D673F">StorageAdapterQueryExtendedInfo</a> function. This member is supported starting in Windows 10.


### -field NotifyDatabaseChange

 


### -field Reserved1

 


### -field Reserved2

 


### -field UpdateRecordBegin

 


### -field UpdateRecordCommit

 




## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/64fb908c-72c2-4639-a2f6-77ede080512c">Plug-in Structures</a>



<a href="https://msdn.microsoft.com/ff7297ee-8d0a-41f4-8abf-66ab5163dae7">WbioQueryStorageInterface</a>
 

 

