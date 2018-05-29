---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.put_ClientName
title: IDiscFormat2TrackAtOnce::put_ClientName
author: windows-sdk-content
description: Sets the friendly name of the client.
old-location: imapi\idiscformat2trackatonce_put_clientname.htm
old-project: imapi
ms.assetid: 9140aa9f-f592-4ef4-85c7-321e5503b0b8
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],put_ClientName method, IDiscFormat2TrackAtOnce.put_ClientName, IDiscFormat2TrackAtOnce::put_ClientName, imapi.idiscformat2trackatonce_put_clientname, imapi2/IDiscFormat2TrackAtOnce::put_ClientName, put_ClientName, put_ClientName method [IMAPI], put_ClientName method [IMAPI],IDiscFormat2TrackAtOnce interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscFormat2TrackAtOnce.put_ClientName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2TrackAtOnce::put_ClientName


## -description


Sets the friendly name of the client. 


## -parameters




### -param value [in]

Name of the client application.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_CLIENT_NAME_IS_NOT_VALID</b></dt>
</dl>
</td>
<td width="60%">
The client name is not valid.

Value: 0xC0AA050F

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
A write operation is in progress.

Value: 0xC0AA0500

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is not valid when media has been "prepared" but not released.

Value: 0xC0AA0503

</td>
</tr>
</table>
 




## -remarks



The name is used when the write operation requests exclusive access to the device. The <a href="https://msdn.microsoft.com/32577b35-235a-4186-8fb3-18e5555cb56f">IDiscRecorder2::get_ExclusiveAccessOwner</a> property contains the name of the client that has the lock.

Because any application with read/write access to the CDROM device during the write operation can use the IOCTL_CDROM_EXCLUSIVE_ACCESS (query) control code (see the Microsoft Windows Driver Development Kit (DDK)) to access the name, it is important that the name identify the program that is using this interface to write to the media. The name is restricted to the same character set as required by the IOCTL_CDROM_EXCLUSIVE_ACCESS control code.




## -see-also




<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>



<a href="https://msdn.microsoft.com/c259233b-4e36-4ee2-8068-d77ece1e927e">IDiscFormat2TrackAtOnce::get_ClientName</a>
 

 

