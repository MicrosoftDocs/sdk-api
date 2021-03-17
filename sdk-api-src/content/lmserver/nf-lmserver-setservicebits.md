---
UID: NF:lmserver.SetServiceBits
title: SetServiceBits function (lmserver.h)
description: Registers a service type with the service control manager and the Server service.
helpviewer_keywords: ["SV_TYPE_AFP","SV_TYPE_BACKUP_BROWSER","SV_TYPE_DIALIN_SERVER","SV_TYPE_DOMAIN_BAKCTRL","SV_TYPE_DOMAIN_CTRL","SV_TYPE_DOMAIN_ENUM","SV_TYPE_DOMAIN_MASTER","SV_TYPE_DOMAIN_MEMBER","SV_TYPE_LOCAL_LIST_ONLY","SV_TYPE_MASTER_BROWSER","SV_TYPE_NOVELL","SV_TYPE_NT","SV_TYPE_POTENTIAL_BROWSER","SV_TYPE_PRINTQ_SERVER","SV_TYPE_SERVER","SV_TYPE_SERVER_UNIX","SV_TYPE_SV_TYPE_SQLSERVER","SV_TYPE_TIME_SOURCE","SV_TYPE_WFW","SV_TYPE_WORKSTATION","SV_TYPE_XENIX_SERVER","SetServiceBits","SetServiceBits function","_win32_setservicebits","base.setservicebits","lmserver/SetServiceBits"]
old-location: base\setservicebits.htm
tech.root: security
ms.assetid: 91a985d4-d1af-4161-ae67-a8a9d6740838
ms.date: 12/05/2018
ms.keywords: SV_TYPE_AFP, SV_TYPE_BACKUP_BROWSER, SV_TYPE_DIALIN_SERVER, SV_TYPE_DOMAIN_BAKCTRL, SV_TYPE_DOMAIN_CTRL, SV_TYPE_DOMAIN_ENUM, SV_TYPE_DOMAIN_MASTER, SV_TYPE_DOMAIN_MEMBER, SV_TYPE_LOCAL_LIST_ONLY, SV_TYPE_MASTER_BROWSER, SV_TYPE_NOVELL, SV_TYPE_NT, SV_TYPE_POTENTIAL_BROWSER, SV_TYPE_PRINTQ_SERVER, SV_TYPE_SERVER, SV_TYPE_SERVER_UNIX, SV_TYPE_SV_TYPE_SQLSERVER, SV_TYPE_TIME_SOURCE, SV_TYPE_WFW, SV_TYPE_WORKSTATION, SV_TYPE_XENIX_SERVER, SetServiceBits, SetServiceBits function, _win32_setservicebits, base.setservicebits, lmserver/SetServiceBits
req.header: lmserver.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetServiceBits
 - lmserver/SetServiceBits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - SetServiceBits
---

# SetServiceBits function


## -description

Registers a service type with the service control manager and the Server service. The Server service can then announce the registered service type as one it currently supports. The 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a> and 
<a href="/windows/desktop/api/lmserver/nf-lmserver-netserverenum">NetServerEnum</a> functions obtain a specified machine's supported service types.

## -parameters

### -param hServiceStatus [in]

A handle to the status information structure for the service. A service obtains the handle by calling the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a> function.

### -param dwServiceBits [in]

The service type. 




Certain bit flags (0xC00F3F7B) are reserved for use by Microsoft. The 
<b>SetServiceBits</b> function fails with the error ERROR_INVALID_DATA if any of these bit flags are set in <i>dwServiceBits</i>. The following bit flags are reserved for use by Microsoft.



#### SV_TYPE_WORKSTATION (0x00000001)



#### SV_TYPE_SERVER (0x00000002)



#### SV_TYPE_DOMAIN_CTRL (0x00000008)



#### SV_TYPE_DOMAIN_BAKCTRL (0x00000010)



#### SV_TYPE_TIME_SOURCE (0x00000020)



#### SV_TYPE_AFP (0x00000040)



#### SV_TYPE_DOMAIN_MEMBER (0x00000100)



#### SV_TYPE_PRINTQ_SERVER (0x00000200)



#### SV_TYPE_DIALIN_SERVER (0x00000400)



#### SV_TYPE_XENIX_SERVER (0x00000800)



#### SV_TYPE_SERVER_UNIX (0x00000800)



#### SV_TYPE_NT (0x00001000)



#### SV_TYPE_WFW (0x00002000)



#### SV_TYPE_POTENTIAL_BROWSER (0x00010000)



#### SV_TYPE_BACKUP_BROWSER (0x00020000)



#### SV_TYPE_MASTER_BROWSER (0x00040000)



#### SV_TYPE_DOMAIN_MASTER (0x00080000)



#### SV_TYPE_LOCAL_LIST_ONLY (0x40000000)



#### SV_TYPE_DOMAIN_ENUM (0x80000000)

Certain bit flags (0x00300084) are defined by Microsoft, but are not specifically reserved for systems software. The following are these bit flags.



#### SV_TYPE_SV_TYPE_SQLSERVER (0x00000004)



#### SV_TYPE_NOVELL (0x00000080)



#### SV_TYPE_DOMAIN_CTRL (0x00100000)



#### SV_TYPE_DOMAIN_BAKCTRL (0x00200000)

Certain bit flags (0x3FC0C000) are not defined by Microsoft, and their use is not coordinated by Microsoft. Developers of applications that use these bits should be aware that other applications can also use them, thus creating a conflict. The following are these bit flags.

<p class="indent">0x00004000

<p class="indent">0x00008000

<p class="indent">0x00400000

<p class="indent">0x00800000

<p class="indent">0x01000000

<p class="indent">0x02000000

<p class="indent">0x04000000

<p class="indent">0x08000000

<p class="indent">0x10000000

<p class="indent">0x20000000

### -param bSetBitsOn [in]

If this value is TRUE, the bits in <i>dwServiceBit</i> are to be set. If this value is FALSE, the bits are to be cleared.

### -param bUpdateImmediately [in]

If this value is TRUE, the Server service is to perform an immediate update. If this value is FALSE, the update is not be performed immediately.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netserverenum">NetServerEnum</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a>