---
UID: NF:imapi2.IWriteEngine2.WriteSection
title: IWriteEngine2::WriteSection
author: windows-sdk-content
description: Writes a data stream to the current recorder.
old-location: imapi\iwriteengine2_writesection.htm
old-project: imapi
ms.assetid: a6158984-04d3-4919-8a67-fc860b4b3a47
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IWriteEngine2 interface [IMAPI],WriteSection method, IWriteEngine2.WriteSection, IWriteEngine2::WriteSection, WriteSection, WriteSection method [IMAPI], WriteSection method [IMAPI],IWriteEngine2 interface, imapi.iwriteengine2_writesection, imapi2/IWriteEngine2::WriteSection
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
-	IWriteEngine2.WriteSection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWriteEngine2::WriteSection


## -description


Writes a data stream to the current recorder.


## -parameters




### -param data [in]

An <b>IStream</b> interface of the data stream to write to the recorder.


### -param startingBlockAddress [in]

Starting logical block address (LBA) of the write operation. Negative values are supported.


### -param numberOfBlocks [in]

Number of blocks from the data stream to write. 


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_REQUEST_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The request was canceled.

Value: 0xC0AA0002

</td>
</tr>
</table>
 




## -remarks



Before calling this method, you must call the <a href="https://msdn.microsoft.com/3ab46d99-7940-4ad0-9772-634de8c0d0ef">IWriteEngine2::put_Recorder</a> method to specify the recording device and the <a href="https://msdn.microsoft.com/aac64c0a-4304-4a20-822e-4aa247d3d9e8">IWriteEngine2::put_BytesPerSector</a> method to specify the number of bytes to use for each sector during writing.

You should also consider calling the following methods if their default values are not appropriate for your application:

<ul>
<li>
<a href="https://msdn.microsoft.com/7060578d-c6d5-4155-9ab8-7185bde38f64">IWriteEngine2::put_EndingSectorsPerSecond</a>
</li>
<li>
<a href="https://msdn.microsoft.com/80d6efdd-c3ce-4c6b-9bc2-7ad34c1dfb5e">IWriteEngine2::put_StartingSectorsPerSecond</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c0fa6248-c582-423d-8983-81cd56d9abdd">IWriteEngine2::put_UseStreamingWrite12</a>
</li>
</ul>
This method is synchronous. To determine the progress of the write operation, you must implement the <a href="https://msdn.microsoft.com/697f8247-6940-4b5e-8521-df89838837be">DWriteEngine2Events</a> interface. For examples that show how to implement an event handler in a script, see <a href="https://msdn.microsoft.com/1f15a5fe-f5d7-4e09-805f-2d0380bf2bb2">Monitoring Progress With Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/697f8247-6940-4b5e-8521-df89838837be">DWriteEngine2Events</a>



<a href="https://msdn.microsoft.com/89e7526f-2b9b-4f37-b537-5046a0ac283d">IWriteEngine2</a>



<a href="https://msdn.microsoft.com/cd658bd3-71ab-4e63-adec-8b7405a76c12">IWriteEngine2::CancelWrite</a>



<a href="https://msdn.microsoft.com/88f67eab-c87b-4a15-b29f-25675d0cac22">IWriteEngine2::get_WriteInProgress</a>



<a href="https://msdn.microsoft.com/b23c81c2-792e-45fc-b862-6daf5b1a6fd1">IWriteEngine2EventArgs::get_SectorCount</a>



<a href="https://msdn.microsoft.com/1c2d1a1f-04b7-4453-af52-4f96e5536ad2">IWriteEngine2EventArgs::get_StartLba</a>
 

 

