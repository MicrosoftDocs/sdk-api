---
UID: NF:winerror.HRESULT_FACILITY
title: HRESULT_FACILITY macro (winerror.h)
description: Extracts the facility of the specified HRESULT.
helpviewer_keywords: ["HRESULT_FACILITY","HRESULT_FACILITY macro [COM]","_com_HRESULT_FACILITY","com.hresult_facility","com.hresult_facility_macro","winerror/HRESULT_FACILITY"]
old-location: com\hresult_facility_macro.htm
tech.root: com
ms.assetid: 35beb1ed-9b63-4e44-a0ae-adaf561e6fd8
ms.date: 12/05/2018
ms.keywords: HRESULT_FACILITY, HRESULT_FACILITY macro [COM], _com_HRESULT_FACILITY, com.hresult_facility, com.hresult_facility_macro, winerror/HRESULT_FACILITY
req.header: winerror.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HRESULT_FACILITY
 - winerror/HRESULT_FACILITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winerror.h
api_name:
 - HRESULT_FACILITY
---

## -description

Extracts the facility of the specified **HRESULT**, which indicates what API or framework originated this error.

## -parameters

### -param hr

The **HRESULT** value.

## -remarks

The facility of an **HRESULT** is stored in bits 16-26 of the **HRESULT**.

This macro is defined as follows:

``` syntax
#define HRESULT_FACILITY(hr)  (((hr) >> 16) & 0x1fff)
```

## Possible values

<!-- List from https://learn.microsoft.com/en-us/archive/blogs/andrew_richards/hresult-facility-by-value -->

| FACILITY                                          | Decimal | Hex   |
|---------------------------------------------------|---------|-------|
| FACILITY_NULL                                     | 0       | 0x0   |
| FACILITY_RPC                                      | 1       | 0x1   |
| FACILITY_DISPATCH                                 | 2       | 0x2   |
| FACILITY_STORAGE                                  | 3       | 0x3   |
| FACILITY_ITF                                      | 4       | 0x4   |
| FACILITY_WIN32                                    | 7       | 0x7   |
| FACILITY_WINDOWS                                  | 8       | 0x8   |
| FACILITY_SECURITY                                 | 9       | 0x9   |
| FACILITY_SSPI                                     | 9       | 0x9   |
| FACILITY_CONTROL                                  | 10      | 0xA   |
| FACILITY_CERT                                     | 11      | 0xB   |
| FACILITY_INTERNET                                 | 12      | 0xC   |
| FACILITY_MEDIASERVER                              | 13      | 0xD   |
| FACILITY_MSMQ                                     | 14      | 0xE   |
| FACILITY_SETUPAPI                                 | 15      | 0xF   |
| FACILITY_SCARD                                    | 16      | 0x10  |
| FACILITY_COMPLUS                                  | 17      | 0x11  |
| FACILITY_AAF                                      | 18      | 0x12  |
| FACILITY_URT                                      | 19      | 0x13  |
| FACILITY_ACS                                      | 20      | 0x14  |
| FACILITY_DPLAY                                    | 21      | 0x15  |
| FACILITY_UMI                                      | 22      | 0x16  |
| FACILITY_SXS                                      | 23      | 0x17  |
| FACILITY_WINDOWS_CE                               | 24      | 0x18  |
| FACILITY_HTTP                                     | 25      | 0x19  |
| FACILITY_USERMODE_COMMONLOG                       | 26      | 0x1A  |
| FACILITY_WER                                      | 27      | 0x1B  |
| FACILITY_USERMODE_FILTER_MANAGER                  | 31      | 0x1F  |
| FACILITY_BACKGROUNDCOPY                           | 32      | 0x20  |
| FACILITY_CONFIGURATION                            | 33      | 0x21  |
| FACILITY_WIA                                      | 33      | 0x21  |
| FACILITY_STATE_MANAGEMENT                         | 34      | 0x22  |
| FACILITY_METADIRECTORY                            | 35      | 0x23  |
| FACILITY_WINDOWSUPDATE                            | 36      | 0x24  |
| FACILITY_DIRECTORYSERVICE                         | 37      | 0x25  |
| FACILITY_GRAPHICS                                 | 38      | 0x26  |
| FACILITY_NAP                                      | 39      | 0x27  |
| FACILITY_SHELL                                    | 39      | 0x27  |
| FACILITY_TPM_SERVICES                             | 40      | 0x28  |
| FACILITY_TPM_SOFTWARE                             | 41      | 0x29  |
| FACILITY_UI                                       | 42      | 0x2A  |
| FACILITY_XAML                                     | 43      | 0x2B  |
| FACILITY_ACTION_QUEUE                             | 44      | 0x2C  |
| FACILITY_PLA                                      | 48      | 0x30  |
| FACILITY_WINDOWS_SETUP                            | 48      | 0x30  |
| FACILITY_FVE                                      | 49      | 0x31  |
| FACILITY_FWP                                      | 50      | 0x32  |
| FACILITY_WINRM                                    | 51      | 0x33  |
| FACILITY_NDIS                                     | 52      | 0x34  |
| FACILITY_USERMODE_HYPERVISOR                      | 53      | 0x35  |
| FACILITY_CMI                                      | 54      | 0x36  |
| FACILITY_USERMODE_VIRTUALIZATION                  | 55      | 0x37  |
| FACILITY_USERMODE_VOLMGR                          | 56      | 0x38  |
| FACILITY_BCD                                      | 57      | 0x39  |
| FACILITY_USERMODE_VHD                             | 58      | 0x3A  |
| FACILITY_SDIAG                                    | 60      | 0x3C  |
| FACILITY_WEBSERVICES                              | 61      | 0x3D  |
| FACILITY_WINPE                                    | 61      | 0x3D  |
| FACILITY_WPN                                      | 62      | 0x3E  |
| FACILITY_WINDOWS_STORE                            | 63      | 0x3F  |
| FACILITY_INPUT                                    | 64      | 0x40  |
| FACILITY_EAP                                      | 66      | 0x42  |
| FACILITY_WINDOWS_DEFENDER                         | 80      | 0x50  |
| FACILITY_OPC                                      | 81      | 0x51  |
| FACILITY_XPS                                      | 82      | 0x52  |
| FACILITY_RAS                                      | 83      | 0x53  |
| FACILITY_MBN                                      | 84      | 0x54  |
| FACILITY_POWERSHELL                               | 84      | 0x54  |
| FACILITY_EAS                                      | 85      | 0x55  |
| FACILITY_P2P_INT                                  | 98      | 0x62  |
| FACILITY_P2P                                      | 99      | 0x63  |
| FACILITY_DAF                                      | 100     | 0x64  |
| FACILITY_BLUETOOTH_ATT                            | 101     | 0x65  |
| FACILITY_AUDIO                                    | 102     | 0x66  |
| FACILITY_VISUALCPP                                | 109     | 0x6D  |
| FACILITY_SCRIPT                                   | 112     | 0x70  |
| FACILITY_PARSE                                    | 113     | 0x71  |
| FACILITY_BLB                                      | 120     | 0x78  |
| FACILITY_BLB_CLI                                  | 121     | 0x79  |
| FACILITY_WSBAPP                                   | 122     | 0x7A  |
| FACILITY_BLBUI                                    | 128     | 0x80  |
| FACILITY_USN                                      | 129     | 0x81  |
| FACILITY_USERMODE_VOLSNAP                         | 130     | 0x82  |
| FACILITY_TIERING                                  | 131     | 0x83  |
| FACILITY_WSB_ONLINE                               | 133     | 0x85  |
| FACILITY_ONLINE_ID                                | 134     | 0x86  |
| FACILITY_DLS                                      | 153     | 0x99  |
| FACILITY_SOS                                      | 160     | 0xA0  |
| FACILITY_DEBUGGERS                                | 176     | 0xB0  |
| FACILITY_USERMODE_SPACES                          | 231     | 0xE7  |
| FACILITY_DMSERVER                                 | 256     | 0x100 |
| FACILITY_RESTORE                                  | 256     | 0x100 |
| FACILITY_SPP                                      | 256     | 0x100 |
| FACILITY_DEPLOYMENT_SERVICES_SERVER               | 257     | 0x101 |
| FACILITY_DEPLOYMENT_SERVICES_IMAGING              | 258     | 0x102 |
| FACILITY_DEPLOYMENT_SERVICES_MANAGEMENT           | 259     | 0x103 |
| FACILITY_DEPLOYMENT_SERVICES_UTIL                 | 260     | 0x104 |
| FACILITY_DEPLOYMENT_SERVICES_BINLSVC              | 261     | 0x105 |
| FACILITY_DEPLOYMENT_SERVICES_PXE                  | 263     | 0x107 |
| FACILITY_DEPLOYMENT_SERVICES_TFTP                 | 264     | 0x108 |
| FACILITY_DEPLOYMENT_SERVICES_TRANSPORT_MANAGEMENT | 272     | 0x110 |
| FACILITY_DEPLOYMENT_SERVICES_DRIVER_PROVISIONING  | 278     | 0x116 |
| FACILITY_DEPLOYMENT_SERVICES_MULTICAST_SERVER     | 289     | 0x121 |
| FACILITY_DEPLOYMENT_SERVICES_MULTICAST_CLIENT     | 290     | 0x122 |
| FACILITY_DEPLOYMENT_SERVICES_CONTENT_PROVIDER     | 293     | 0x125 |
| FACILITY_LINGUISTIC_SERVICES                      | 305     | 0x131 |
| FACILITY_WEB                                      | 885     | 0x375 |
| FACILITY_WEB_SOCKET                               | 886     | 0x376 |
| FACILITY_AUDIOSTREAMING                           | 1094    | 0x446 |
| FACILITY_ACCELERATOR                              | 1536    | 0x600 |
| FACILITY_MOBILE                                   | 1793    | 0x701 |
| FACILITY_WMAAECMA                                 | 1996    | 0x7CC |
| FACILITY_WEP                                      | 2049    | 0x801 |
| FACILITY_SYNCENGINE                               | 2050    | 0x802 |
| FACILITY_DIRECTMUSIC                              | 2168    | 0x878 |
| FACILITY_DIRECT3D10                               | 2169    | 0x879 |
| FACILITY_DXGI                                     | 2170    | 0x87A |
| FACILITY_DXGI_DDI                                 | 2171    | 0x87B |
| FACILITY_DIRECT3D11                               | 2172    | 0x87C |
| FACILITY_LEAP                                     | 2184    | 0x888 |
| FACILITY_AUDCLNT                                  | 2185    | 0x889 |
| FACILITY_WINCODEC_DWRITE_DWM                      | 2200    | 0x898 |
| FACILITY_DIRECT2D                                 | 2201    | 0x899 |
| FACILITY_DEFRAG                                   | 2304    | 0x900 |
| FACILITY_USERMODE_SDBUS                           | 2305    | 0x901 |
| FACILITY_JSCRIPT                                  | 2306    | 0x902 |
| FACILITY_PIDGENX                                  | 2561    | 0xA01 |

## -see-also

<a href="/windows/desktop/com/error-handling-in-com">Error Handling</a>
