---
UID: NF:mswmdm.IMDSPObject.Close
title: IMDSPObject::Close
author: windows-sdk-content
description: The Close method closes a file on a storage medium of a media device.
old-location: wmdm\imdspobject_close.htm
tech.root: WMDM
ms.assetid: 453dbf9e-4b71-4ceb-80e2-eaa0cf4cd29d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Close, Close method [windows Media Device Manager], Close method [windows Media Device Manager],IMDSPObject interface, IMDSPObject interface [windows Media Device Manager],Close method, IMDSPObject.Close, IMDSPObject::Close, IMDSPObjectClose, mswmdm/IMDSPObject::Close, wmdm.imdspobject_close
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMDSPObject.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mswmdm.h
: 
- IMDSPObject.Close
: 
---

# IMDSPObject::Close


## -description



The <b>Close</b> method closes a file on a storage medium of a media device.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/271d7185-1a9d-4bec-9289-4ae5461ed741">IMDSPObject Interface</a>



<a href="https://msdn.microsoft.com/9e54bcbd-4f14-49e0-8211-2f79f024c80a">IMDSPObject::Open</a>



<a href="https://msdn.microsoft.com/1acf4112-0cb8-47e4-b8dc-3e820c0ef72f">IMDSPObject::Read</a>



<a href="https://msdn.microsoft.com/29f16be5-9304-4b09-86e8-3f9e0e591a41">IMDSPObject::Write</a>
 

 

