---
UID: NS:winbio_adapter._WINBIO_STORAGE_RECORD
title: WINBIO_STORAGE_RECORD
author: windows-sdk-content
description: Contains a biometric template and associated data in a standard format.
old-location: secbiomet\winbio_storage_record.htm
tech.root: SecBioMet
ms.assetid: fd638a08-cff0-4984-8580-a1eecd509a1f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWINBIO_STORAGE_RECORD, PWINBIO_STORAGE_RECORD, PWINBIO_STORAGE_RECORD structure pointer [Windows Biometric Framework API], WINBIO_STORAGE_RECORD, WINBIO_STORAGE_RECORD structure [Windows Biometric Framework API], secbiomet.winbio_storage_record, winbio_adapter/PWINBIO_STORAGE_RECORD, winbio_adapter/WINBIO_STORAGE_RECORD"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio_adapter.h
api_name:
 - WINBIO_STORAGE_RECORD
product: Windows
targetos: Windows
req.typenames: WINBIO_STORAGE_RECORD, *PWINBIO_STORAGE_RECORD
req.redist: 
---

# WINBIO_STORAGE_RECORD structure


## -description


The <b>WINBIO_STORAGE_RECORD</b> structure contains a biometric template and associated data in a standard format. This structure is used to pass information between an engine adapter and a storage adapter.


## -struct-fields




### -field Identity

Pointer to a  <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure that contains the GUID or SID of the storage record.


### -field SubFactor

A <a href="https://msdn.microsoft.com/019569A9-6184-4E75-9B82-C98F4F45F61A">WINBIO_BIOMETRIC_SUBTYPE</a> value that specifies the biometric sub-factor associated with the template data.

<div class="alert"><b>Important</b>  <p class="note">Do not attempt to validate the value supplied for the <i>SubFactor</i> value. The Windows Biometrics Service will validate the supplied value before passing it through to your implementation. If the value is <b>WINBIO_SUBTYPE_NO_INFORMATION</b> or <b>WINBIO_SUBTYPE_ANY</b>, then validate where appropriate.

</div>
<div> </div>

### -field IndexVector

Pointer to a contiguous array of <b>ULONG</b> values. These values represent the bucket address assigned to the biometric template by the engine adapter.


### -field IndexElementCount

The number of <b>ULONG</b> values in the array specified by the <i>IndexVector</i> field.


### -field TemplateBlob

Pointer to an array of bytes that contains the biometric template data.


### -field TemplateBlobSize

Size, in bytes, of the template specified by the <i>TemplateBlob</i> parameter.


### -field PayloadBlob

Pointer to an array of bytes that contains integrity checking data. This field is used only by adapters for removable devices that contain embedded storage.


### -field PayloadBlobSize

Size, in bytes, of the data specified by the <i>PayloadBlob</i> parameter.


## -remarks



The <b>WINBIO_STORAGE_RECORD</b> structure and the memory it points to are the property of the component that created the structure. In particular, the component determines when the structure is deleted and when its embedded pointers become invalid. When other components are given temporary access to this structure, they must follow the rules  governing structure  lifetime set by the owning component.




## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/64fb908c-72c2-4639-a2f6-77ede080512c">Plug-in Structures</a>



<a href="https://msdn.microsoft.com/a06550da-c6ea-44e5-b54f-8005bcbc0364">StorageAdapterGetCurrentRecord</a>
 

 

