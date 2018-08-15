---
UID: NF:mswmdm.IMDSPObject.Read
title: IMDSPObject::Read
author: windows-sdk-content
description: The Read method reads data from the object at the current position. This operation is valid only if the storage object represents a file.
old-location: wmdm\imdspobject_read.htm
old-project: WMDM
ms.assetid: 1acf4112-0cb8-47e4-b8dc-3e820c0ef72f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMDSPObject interface [windows Media Device Manager],Read method, IMDSPObject.Read, IMDSPObject::Read, IMDSPObjectRead, Read, Read method [windows Media Device Manager], Read method [windows Media Device Manager],IMDSPObject interface, mswmdm/IMDSPObject::Read, wmdm.imdspobject_read
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPObject.Read
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPObject::Read


## -description



The <b>Read</b> method reads data from the object at the current position. This operation is valid only if the storage object represents a file.




## -parameters




### -param pData [out]

Pointer to a buffer to receive the data read from the object. This parameter is included in the output message authentication code and must be encrypted using <a href="https://msdn.microsoft.com/dbfc72a6-acd5-40c2-8951-ab90e5c4d752">CSecureChannelServer::EncryptParam</a>. See Remarks.


### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> specifying the number of bytes of data to read. Upon return, this parameter contains the actual amount of data read. This parameter must be included in the input message authentication code.


### -param abMac






#### - abMac[WMDM_MAC_LENGTH] [in, out]

Array of eight bytes containing the message authentication code for the parameter data of this method. (WMDM_MAC_LENGTH is defined as 8.)


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The MAC used for encryption should include both <i>pData</i> and <i>pdwSize</i> in calls to <a href="https://msdn.microsoft.com/f8b5548d-ffd5-4dc3-8d08-61a65841a997">CSecureChannelServer::MACUpdate</a>.

This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/6aef4138-0391-4edd-b4fc-d6d0ec3c735b">Encryption and Decryption</a>



<a href="https://msdn.microsoft.com/271d7185-1a9d-4bec-9289-4ae5461ed741">IMDSPObject Interface</a>



<a href="https://msdn.microsoft.com/453dbf9e-4b71-4ceb-80e2-eaa0cf4cd29d">IMDSPObject::Close</a>



<a href="https://msdn.microsoft.com/9e54bcbd-4f14-49e0-8211-2f79f024c80a">IMDSPObject::Open</a>



<a href="https://msdn.microsoft.com/89494180-9dd7-41f3-b510-a59c38415d75">IMDSPObject::Seek</a>



<a href="https://msdn.microsoft.com/29f16be5-9304-4b09-86e8-3f9e0e591a41">IMDSPObject::Write</a>
 

 

