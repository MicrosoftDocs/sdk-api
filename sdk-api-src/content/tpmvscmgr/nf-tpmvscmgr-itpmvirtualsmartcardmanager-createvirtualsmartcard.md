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

# ITpmVirtualSmartCardManager::CreateVirtualSmartCard


## -description


Creates a TPM virtual smart card with the given parameters.


## -parameters




### -param pszFriendlyName [in]

Display name of the smart card reader node. This is shown in the Device Manager, but it is not the reader name as seen by the smart card resource manager (SCRM).


### -param bAdminAlgId [in]

Algorithm identifier of the admin key. Currently, to work with the inbox GIDS minidriver, this value should be VSC_DEFAULT_ADMIN_ALGORITHM_ID (3-key triple DES with ISO/IEC 9797 padding method 2 in CBC chaining mode).


### -param pbAdminKey [in]

Pointer to a byte array that contains the admin key of the virtual smart card to be created. 


### -param cbAdminKey [in]

Size, in bytes, of the byte array pointed to by the <i>pbAdminKey</i> parameter. 


### -param pbAdminKcv [in, optional]

Pointer to a byte array that contains the key check value of the admin key. Key check value is defined as the first 3 bytes of the output BLOB when using the admin key to encrypt a block of zeros. If the key check value is not provided, there will be no integrity check for the admin key. 


### -param cbAdminKcv [in]

Size, in bytes, of the byte array pointed to by the <i>pbAdminKcv</i> parameter.


### -param pbPuk [in, optional]

Pointer to a byte array that contains the PIN unlock key (PUK) value of the virtual smart card. It is usually a sequence of ASCII characters with a minimal length of 8 characters. If the PUK is not provided, the virtual smart card will be created without a PUK role and instead will use the challenge/response-based PIN reset through the admin role.


### -param cbPuk [in]

Size, in bytes, of the byte array pointed to by the <i>pbPuk</i> parameter.


### -param pbPin [in]

Pointer to a byte array that contains the PIN value of the virtual smart card. It is usually a sequence of ASCII characters with a length of 8 characters minimum and 127 characters maximum.


### -param cbPin [in]

Size, in bytes, of the byte array pointed to by the <i>pbPin</i> parameter.


### -param fGenerate [in]

Indicates whether the virtual smart card needs to be provisioned with all necessary files required by the base CSP and smart card KSP.


### -param pStatusCallback [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/6CB62E42-16FD-453F-9566-B4DFCDAC7368">ITpmVirtualSmartCardManagerStatusCallback</a> interface. The TPM virtual smart card manager uses this callback interface to communicate the progress or error during virtual smart card creation. If the <i>pStatusCallback</i> parameter is <b>NULL</b>, no progress is reported to the client before the operation completes.


### -param ppszInstanceId [out]

Pointer to a pointer to a Unicode buffer to receive the instance ID of the created virtual smart card.


### -param pfNeedReboot [out]

Pointer to a Boolean value to receive whether the requested operation needs to reboot the computer.


## -returns



If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns a Win32 error code. 




## -remarks



When the method succeeds, the <i>ppszInstanceId</i> parameter points to the Unicode buffer that contains the instance identifier of the newly created TPM virtual smart card reader. When you have finished using the buffer, the caller needs to free the buffer on the client by calling the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function, as directed in the COM memory management rules.




## -see-also




<a href="https://msdn.microsoft.com/46CC703B-14A2-4588-BA13-837C76B70F07">ITpmVirtualSmartCardManager</a>
 

 

