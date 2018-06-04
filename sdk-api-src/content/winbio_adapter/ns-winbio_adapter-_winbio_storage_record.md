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

# _WINBIO_STORAGE_RECORD structure


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
 

 

