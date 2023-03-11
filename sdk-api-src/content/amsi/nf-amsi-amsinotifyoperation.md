---
UID: NF:amsi.AmsiNotifyOperation
title: AmsiNotifyOperation
description: Sends to the antimalware provider a notification of an arbitrary operation. (AmsiNotifyOperation)
tech.root: AMSI
ms.date: 01/08/2021
req.construct-type: function
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AmsiNotifyOperation
 - amsi/AmsiNotifyOperation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - amsi.dll
api_name:
 - AmsiNotifyOperation
---

## -description

Sends to the antimalware provider a notification of an arbitrary operation. The notification doesn't imply the request of an antivirus scan. Rather, **IAntimalwareProvider2::Notify** is designed to provide a quick and lightweight mechanism to communicate to the antimalware provider that an event has taken place. In general, the antimalware provider should process the notification, and return to the caller as quickly as possible.

## -parameters

### -param amsiContext

Type: \_In\_ **HAMSICONTEXT**

The handle (of type **HAMSICONTEXT**) that was initially received from [AmsiInitialize](./nf-amsi-amsiinitialize.md).

### -param buffer

Type: \_In\_reads\_bytes\_(length) **[PVOID](/windows/win32/winprog/windows-data-types)**

The buffer that contains the notification data.

### -param length

Type: \_In\_ **[ULONG](/windows/win32/winprog/windows-data-types)**

The length, in bytes, of the data to be read from *buffer*.

### -param contentName

Type: \_In\_opt\_ **[LPCWSTR](/windows/win32/winprog/windows-data-types)**

The filename, URL, unique script ID, or similar of the content being scanned.

### -param result

Type: \_Out\_ **[AMSI_RESULT](/windows/win32/api/amsi/ne-amsi-amsi_result)\***

The result of the scan.

You should use [AmsiResultIsMalware](/windows/win32/api/amsi/nf-amsi-amsiresultismalware) to determine whether the content should be blocked.

## -returns

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

## -see-also
