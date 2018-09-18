---
UID: NF:winscard.SCardGetReaderIconW
title: SCardGetReaderIconW function
author: windows-sdk-content
description: Gets an icon of the smart card reader for a given reader's name.
old-location: security\scardgetreadericon.htm
tech.root: secauthn
ms.assetid: A83B5AF3-BF2C-42AE-9D34-3B651D7AF047
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: SCardGetReaderIcon, SCardGetReaderIcon function [Security], SCardGetReaderIconA, SCardGetReaderIconW, security.scardgetreadericon, winscard/SCardGetReaderIcon
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winscard.h
api_name:
 - SCardGetReaderIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardGetReaderIconW function


## -description


The <b>SCardGetReaderIcon</b> function gets an icon of the smart card reader for a given reader's name. This function does not affect the state of the card reader.


## -parameters




### -param hContext [in]

Handle that identifies the resource manager context for the query. You can set the resource manager context by a previous call to the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function. This parameter cannot be <b>NULL</b>.


### -param szReaderName [in]

Reader name. You can get this value by calling the <a href="https://msdn.microsoft.com/b50218f1-e960-4838-b44b-6c71fa94a0ad">SCardListReaders</a> function.


### -param pbIcon [out]

Pointer to a buffer that contains a BLOB of the smart card reader icon as read from the icon file. If this value is <b>NULL</b>, the function ignores the buffer length supplied in the <i>pcbIcon</i> parameter, writes the length of the buffer that would have been returned to <i>pcbIcon</i> if this parameter had not been NULL, and returns a success code.


### -param pcbIcon [in, out]

Length, in characters, of the <i>pbIcon</i> buffer. This parameter receives the actual length of the received attribute. If the buffer length is specified as SCARD_AUTOALLOCATE, then <i>pbIcon</i> is converted from a pointer to a byte pointer and receives the address of a block of memory that contains the attribute. This block of memory must be deallocated with the <a href="https://msdn.microsoft.com/d41d3891-671b-4129-8034-b251af983830">SCardFreeMemory</a> function.


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
<a href="https://msdn.microsoft.com/en-us/library/Aa374738(v=VS.85).aspx">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



The icon should be 256 × 256 pixels with no alpha channel.  


#### Examples


```cpp
PBYTE    pbIcon = NULL;
DWORD    cbIcon = SCARD_AUTOALLOCATE;
DWORD    i;
LONG     lReturn;
LPTSTR   szReaderName = "USB Smart Card Reader 0";

// Retrieve the reader's icon.
// hContext was set by a previous call to SCardEstablishContext.
lReturn = SCardGetReaderIcon(hContext,
                         szReaderName,
                         (PBYTE)&pbIcon,
                         &cbIcon);

if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardGetReaderIcon - %x\n", lReturn);
    // Take appropriate action.
}
else
{
    // Free the memory when done. 
    lReturn = SCardFreeMemory(hContext, pbIcon);
}

```




