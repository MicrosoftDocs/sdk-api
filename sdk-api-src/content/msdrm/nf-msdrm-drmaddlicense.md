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

# DRMAddLicense function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMAddLicense</b> function adds an end-user license to the temporary or permanent license store.


## -parameters




### -param hLicenseStorage [in]

A handle to a license storage session, created using <a href="https://msdn.microsoft.com/6561b6df-373b-4bd3-9196-09ef945f8042">DRMCreateLicenseStorageSession</a>.


### -param uFlags [in]

Value that specifies whether the temporary or permanent license store is used. This parameter can be one of the following values.



#### DRM_ADD_LICENSE_NOPERSIST

The end-user license is added to the temporary license store.



#### DRM_ADD_LICENSE_PERSIST

The end-user license is added to the permanent license store.


### -param wszLicense [in]

A pointer to null-terminated string that contains the end-user license chain to add to the temporary or permanent license store.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



An application can manage its own end-user licenses instead of submitting them to the computer's permanent license store. To do so, the application calls <a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a> with <b>DRM_AL_NOPERSIST</b> specified. The application then retrieves the license from the license store using <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a>, deletes the license from the license store using <a href="https://msdn.microsoft.com/596f9959-0beb-4051-87c4-b8704abd8fc0">DRMDeleteLicense</a>, and saves the end-user license itself. The temporary license store is destroyed when the reader session ends. To use the license the next time, the application must add it to the temporary license store using this function. <b>DRMAddLicense</b> can be called multiple times to add multiple licenses to the temporary license store.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a>
 

 

