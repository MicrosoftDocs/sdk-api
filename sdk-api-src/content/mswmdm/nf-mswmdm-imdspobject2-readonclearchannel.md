---
UID: NF:mswmdm.IMDSPObject2.ReadOnClearChannel
title: IMDSPObject2::ReadOnClearChannel (mswmdm.h)
author: windows-sdk-content
description: The ReadOnClearChannel method reads data from the object at the current position without using secure authenticated channels.
old-location: wmdm\imdspobject2_readonclearchannel.htm
tech.root: WMDM
ms.assetid: a7ccf074-e033-46e4-a7ce-d0086f4b1dc9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPObject2 interface [windows Media Device Manager],ReadOnClearChannel method, IMDSPObject2.ReadOnClearChannel, IMDSPObject2::ReadOnClearChannel, IMDSPObject2ReadOnClearChannel, ReadOnClearChannel, ReadOnClearChannel method [windows Media Device Manager], ReadOnClearChannel method [windows Media Device Manager],IMDSPObject2 interface, mswmdm/IMDSPObject2::ReadOnClearChannel, wmdm.imdspobject2_readonclearchannel
ms.topic: method
req.header: mswmdm.h
req.include-header: 
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPObject2.ReadOnClearChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPObject2::ReadOnClearChannel


## -description



The <b>ReadOnClearChannel</b> method reads data from the object at the current position without using secure authenticated channels. This is still secure for use with DRM-protected content. This operation is valid only if the storage object represents a file. If <b>IMDSPObject2</b> is supported, this method must be implemented. Windows Media Device Manager does not fall back to <a href="https://msdn.microsoft.com/1acf4112-0cb8-47e4-b8dc-3e820c0ef72f">IMDSPObject::Read</a> if this method fails.




## -parameters




### -param pData [out]

Pointer to a buffer to receive the data read from the object.


### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> specifying the number of bytes of data to read. Upon return, this parameter contains the actual amount of data read.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method can be used for DRM-protected content. This method is more efficient than <a href="https://msdn.microsoft.com/1acf4112-0cb8-47e4-b8dc-3e820c0ef72f">IMDSPObject::Read</a> because this method does not involve encrypting and decrypting parameters.




## -see-also




<a href="https://msdn.microsoft.com/a312dfef-ac48-4c58-a59a-b277f5386419">Enabling Synchronization with Windows Media Player</a>



<a href="https://msdn.microsoft.com/f79c07a6-b7e6-4c00-83be-ac2bfc9a751b">IMDSPObject2 Interface</a>



<a href="https://msdn.microsoft.com/9c80f382-2536-4f08-9111-94ad757747f7">IMDSPObject2::WriteOnClearChannel</a>



<a href="https://msdn.microsoft.com/1acf4112-0cb8-47e4-b8dc-3e820c0ef72f">IMDSPObject::Read</a>
 

 

