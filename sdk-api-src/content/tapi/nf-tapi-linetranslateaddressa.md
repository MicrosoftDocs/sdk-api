---
UID: NF:tapi.lineTranslateAddressA
title: lineTranslateAddressA function
author: windows-sdk-content
description: The lineTranslateAddress function translates the specified address into another format.
old-location: tapi2\linetranslateaddress.htm
tech.root: tapi
ms.assetid: 0347d526-9596-4b42-8075-07318bf39634
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_tapi2_linetranslateaddress, lineTranslateAddress, lineTranslateAddress function [TAPI 2.2], lineTranslateAddressA, lineTranslateAddressW, tapi/lineTranslateAddress, tapi/lineTranslateAddressA, tapi/lineTranslateAddressW, tapi2.linetranslateaddress"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineTranslateAddressW (Unicode) and lineTranslateAddressA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
 - Ext-MS-Win-ras-tapi32-l1-1-0.dll
api_name:
 - lineTranslateAddress
 - lineTranslateAddressA
 - lineTranslateAddressW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- lineTranslateAddressA
: 
---

# lineTranslateAddressA function


## -description


The 
<b>lineTranslateAddress</b> function translates the specified address into another format.


## -parameters




### -param hLineApp

Handle returned by 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>. If a TAPI 2.x application has not yet called the 
<b>lineInitializeEx</b> function, it can set this parameter to <b>NULL</b>. TAPI 1.4 applications must still call 
<a href="https://msdn.microsoft.com/4b406f19-be9b-4130-91a7-5fdfa56f7fc3">lineInitialize</a> first.


### -param dwDeviceID

Device identifier of the line device upon which the call is to be dialed, so that variations in dialing procedures on different lines can be applied to the translation process.


### -param dwAPIVersion

Highest version of TAPI supported by the application (not necessarily the value negotiated by 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> on some particular line device).


### -param lpszAddressIn

Pointer to a <b>null</b>-terminated string that contains the address of the information that is to be extracted for translation. Must be in either the canonical address format, or an arbitrary string of dialable digits (non-canonical). This parameter must not be <b>NULL</b>. If the <i>AddressIn</i> contains a subaddress or name field, or additional addresses separated from the first address by CR and LF characters, only the first address is translated.


### -param dwCard

Credit card to be used for dialing. This parameter is only valid if the CARDOVERRIDE bit is set in <i>dwTranslateOptions</i>. This parameter specifies the permanent identifier of a Card entry in the [Cards] section in the registry (as obtained from 
<a href="https://msdn.microsoft.com/9b4dcbe6-41e9-4b9c-9150-d0c7edef5a19">lineTranslateCaps</a>) that should be used instead of the <b>PreferredCardID</b> specified in the definition of the <b>CurrentLocation</b>. It does not cause the <i>PreferredCardID</i> parameter of the current Location entry in the registry to be modified; the override applies only to the current translation operation. This parameter is ignored if the CARDOVERRIDE bit is not set in <i>dwTranslateOptions</i>.


### -param dwTranslateOptions

Associated operations to be performed prior to the translation of the address into a dialable string. This parameter uses one of the 
<a href="https://msdn.microsoft.com/3f5e9952-945e-42b8-8536-b52a0c833282">LINETRANSLATEOPTION_ Constants</a>. 




If you have set the LINETRANSLATEOPTION_CANCELCALLWAITING bit, it is also advisable to set the LINECALLPARAMFLAGS_SECURE bit in the <b>dwCallParamFlags</b> member of the 
<a href="https://msdn.microsoft.com/e7bc5604-20eb-48d8-a857-df8962c6b2ae">LINECALLPARAMS</a> structure (passed in to 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> through the <i>lpCallParams</i> parameter). This prevents the line device from using dialable digits to suppress call interrupts.


### -param lpTranslateOutput

Pointer to an application-allocated memory area to contain the output of the translation operation, of type 
<a href="https://msdn.microsoft.com/bcf094ad-8098-4e45-9131-25dbdb7e4093">LINETRANSLATEOUTPUT</a>. Prior to calling 
<b>lineTranslateAddress</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_INVALPOINTER, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NODRIVER, LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALADDRESS, LINEERR_OPERATIONFAILED, LINEERR_INVALAPPHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALCARD, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALPARAM.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="../tapi3/address_ovr.htm">Canonical Addresses</a>



<a href="https://msdn.microsoft.com/e7bc5604-20eb-48d8-a857-df8962c6b2ae">LINECALLPARAMS</a>



<a href="https://msdn.microsoft.com/bcf094ad-8098-4e45-9131-25dbdb7e4093">LINETRANSLATEOUTPUT</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/36a17ae8-31db-4db9-a401-097d47aa26ad">TAPI Version Negotiation</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>



<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>
 

 

