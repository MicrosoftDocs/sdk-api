---
UID: NF:winscard.SCardIntroduceReaderW
title: SCardIntroduceReaderW function
author: windows-sdk-content
description: Introduces a new name for an existing smart card reader.
old-location: security\scardintroducereader.htm
tech.root: secauthn
ms.assetid: 1f8b9d75-5bba-40c3-99a0-6910855fcd4d
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: SCardIntroduceReader, SCardIntroduceReader function [Security], SCardIntroduceReaderA, SCardIntroduceReaderW, _smart_scardintroducereader, security.scardintroducereader, winscard/SCardIntroduceReader, winscard/SCardIntroduceReaderA, winscard/SCardIntroduceReaderW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardIntroduceReaderW (Unicode) and SCardIntroduceReaderA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardIntroduceReader
 - SCardIntroduceReaderA
 - SCardIntroduceReaderW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardIntroduceReaderW function


## -description


The <b>SCardIntroduceReader</b> function introduces a new name for an existing <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a>.
<div class="alert"><b>Note</b>  Smart card readers are automatically introduced to the system; a smart card reader vendor's setup program can also introduce a smart card reader to the system.</div><div> </div>

## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.


### -param szReaderName [in]

Display name to be assigned to the reader.


### -param szDeviceName [in]

System name of the smart card reader, for example, "MyReader 01".


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



All readers installed on the system are automatically introduced by their system name. Typically, <b>SCardIntroduceReader</b> is called only to change the name of an existing reader.

The <b>SCardIntroduceReader</b> function is a database management function. For more information on other database management functions, see 
<a href="https://msdn.microsoft.com/a2f457e1-c042-42e7-9071-cf0edd68e27a">Smart Card Database Management Functions</a>.

To remove a reader, use 
<a href="https://msdn.microsoft.com/2022caff-ba01-4d0d-977c-3f51bde95659">SCardForgetReader</a>.


#### Examples

The following example  shows introducing a smart card reader.


```cpp
// This example renames the reader name.
// This is a two-step process (first add the new
// name, then forget the old name).
LPBYTE    pbAttr = NULL;
DWORD     cByte = SCARD_AUTOALLOCATE;
LONG      lReturn;

// Step 1: Add the new reader name.
// The device name attribute is a necessary value.
// hCardHandle was set by a previous call to SCardConnect.
lReturn = SCardGetAttrib(hCardHandle,
                         SCARD_ATTR_DEVICE_SYSTEM_NAME,
                         (LPBYTE)&pbAttr,
                         &cByte);
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardGetAttrib\n");
    exit(1);  // Or other error action
}
// Add the reader name.
// hContext was set earlier by SCardEstablishContext.
lReturn = SCardIntroduceReader(hContext,
                               TEXT("My New Reader Name"),
                               (LPCTSTR)pbAttr );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardIntroduceReader\n");
    exit(1);  // Or other error action
}

// Step 2: Forget the old reader name.
lReturn = SCardForgetReader(hContext,
                            (LPCTSTR)pbAttr );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardForgetReader\n");
    exit(1);  // Or other error action
}

// Free the memory when done.
lReturn = SCardFreeMemory( hContext, pbAttr );

```





## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/2022caff-ba01-4d0d-977c-3f51bde95659">SCardForgetReader</a>



<a href="https://msdn.microsoft.com/1ac88466-1277-44d7-a471-b31d6bfce99e">SCardIntroduceCardType</a>



<a href="https://msdn.microsoft.com/aaf7d2f9-71d5-42bb-a96f-71124be40aa3">SCardIntroduceReaderGroup</a>
 

 

