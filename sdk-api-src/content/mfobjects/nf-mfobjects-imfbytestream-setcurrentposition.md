---
UID: NF:mfobjects.IMFByteStream.SetCurrentPosition
title: IMFByteStream::SetCurrentPosition
author: windows-driver-content
description: Sets the current read or write position.
old-location: mf\imfbytestream_setcurrentposition.htm
old-project: medfound
ms.assetid: 20518fed-4083-413b-b9b1-e54c4c5630d4
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: 20518fed-4083-413b-b9b1-e54c4c5630d4, IMFByteStream interface [Media Foundation],SetCurrentPosition method, IMFByteStream.SetCurrentPosition, IMFByteStream::SetCurrentPosition, SetCurrentPosition, SetCurrentPosition method [Media Foundation], SetCurrentPosition method [Media Foundation],IMFByteStream interface, mf.imfbytestream_setcurrentposition, mfobjects/IMFByteStream::SetCurrentPosition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFByteStream.SetCurrentPosition
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStream::SetCurrentPosition


## -description



Sets the current read or write position.




## -parameters




### -param qwPosition [in]

New position in the stream, as a byte offset from the start of the stream.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

                Invalid argument.
              

</td>
</tr>
</table>
 




## -remarks




        If the new position is larger than the length of the stream, the method returns E_INVALIDARG.
      

<b> Implementation notes:</b>
This method should update the current position in the stream by setting the current position to the value passed in to the <i>qwPosition</i> parameter. Other methods that can update the current position are <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>, <a href="https://msdn.microsoft.com/ed4aaf2a-270c-4518-b04d-cdac966bf9a5">BeginRead</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a>, <a href="https://msdn.microsoft.com/078a8ffe-7b4f-487e-8655-fe5ea14ba306">BeginWrite</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>.


This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>
 

 

