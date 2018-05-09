---
UID: NF:winscard.SCardGetDeviceTypeIdA
title: SCardGetDeviceTypeIdA function
author: windows-driver-content
description: Gets the device type identifier of the card reader for the given reader name. This function does not affect the state of the reader.
old-location: security\scardgetdevicetypeid.htm
old-project: SecAuthN
ms.assetid: E637B5D6-B605-4216-9581-7E4ADC75F75A
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: SCardGetDeviceTypeId, SCardGetDeviceTypeId function [Security], SCardGetDeviceTypeIdA, SCardGetDeviceTypeIdW, security.scardgetdevicetypeid, winscard/SCardGetDeviceTypeId, winscard/SCardGetDeviceTypeIdA, winscard/SCardGetDeviceTypeIdW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardGetDeviceTypeIdW (Unicode) and SCardGetDeviceTypeIdA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winscard.dll
api_name:
-	SCardGetDeviceTypeId
-	SCardGetDeviceTypeIdA
-	SCardGetDeviceTypeIdW
product: Windows
targetos: Windows
req.lib: 
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardGetDeviceTypeIdA function


## -description


The <b>SCardGetDeviceTypeId</b> function gets the device type identifier of the card reader for the given reader name. This function does not affect the state of the reader.


## -parameters




### -param hContext [in]

Handle that identifies the resource manager context for the query. You can set the resource manager context by calling the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function. This parameter cannot be NULL.


### -param szReaderName [in]

Reader name. You can get this value by calling the <a href="https://msdn.microsoft.com/b50218f1-e960-4838-b44b-6c71fa94a0ad">SCardListReaders</a> function.


### -param pdwDeviceTypeId [in, out]

The actual device type identifier. The list of reader types returned by this function are listed under <b>ReaderType</b> member in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548930">SCARD_READER_CAPABILITIES</a> structure.


## -returns



This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 



