---
UID: NF:xenroll.IEnroll2.put_HashAlgID
title: IEnroll2::put_HashAlgID
author: windows-sdk-content
description: The HashAlgID property of IEnroll4 sets or retrieves the hash algorithm used when signing a PKCS #10 certificate request.
old-location: security\ienroll4_hashalgid.htm
tech.root: seccrypto
ms.assetid: ebf4a7c7-4bd4-4a5f-8f32-bb30a6a8af0e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: HashAlgID property [Security], HashAlgID property [Security],IEnroll2 interface, HashAlgID property [Security],IEnroll4 interface, IEnroll2 interface [Security],HashAlgID property, IEnroll2.HashAlgID, IEnroll2.put_HashAlgID, IEnroll2::HashAlgID, IEnroll2::get_HashAlgID, IEnroll2::put_HashAlgID, IEnroll4 interface [Security],HashAlgID property, IEnroll4.HashAlgID, IEnroll4::get_HashAlgID, IEnroll4::put_HashAlgID, get_HashAlgID, put_HashAlgID, security.ienroll4_hashalgid, xenroll/IEnroll2::HashAlgID, xenroll/IEnroll2::get_HashAlgID, xenroll/IEnroll2::put_HashAlgID, xenroll/IEnroll4::HashAlgID, xenroll/IEnroll4::get_HashAlgID, xenroll/IEnroll4::put_HashAlgID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll2.HashAlgID
 - IEnroll2.get_HashAlgID
 - IEnroll2.put_HashAlgID
 - IEnroll4.HashAlgID
 - IEnroll4.get_HashAlgID
 - IEnroll4.put_HashAlgID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll2::put_HashAlgID


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>HashAlgID</b> property sets or retrieves the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash algorithm</a> used when signing a PKCS #10 <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.

This property was first introduced in the <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a> interface.

This property is read/write.


## -parameters


## -remarks



The values for this property are <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash algorithm</a> IDs, such as those returned by the 
<a href="https://msdn.microsoft.com/a40d85d0-fd02-4e0a-af7d-dfefe02f4e2a">EnumAlgs</a> method. If both the <b>HashAlgID</b> and 
<a href="https://msdn.microsoft.com/c359c4c8-f53d-48f1-a2ac-9275751b48dc">HashAlgorithmWStr</a> properties are set, whichever has been updated most recently determines the hash algorithm used to sign the PKCS #10 request.




## -see-also




<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>



<a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a>



<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

