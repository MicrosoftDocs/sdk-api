---
UID: NF:wmsdkidl.IWMAddressAccess.GetAccessEntryCount
title: IWMAddressAccess::GetAccessEntryCount
author: windows-driver-content
description: The GetAccessEntryCount method retrieves the number of entries in the IP address access list.
old-location: wmformat\iwmaddressaccess_getaccessentrycount.htm
old-project: wmformat
ms.assetid: 996d8a8a-887e-4e2f-b810-c57a4251f771
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetAccessEntryCount, GetAccessEntryCount method [windows Media Format], GetAccessEntryCount method [windows Media Format],IWMAddressAccess interface, IWMAddressAccess interface [windows Media Format],GetAccessEntryCount method, IWMAddressAccess.GetAccessEntryCount, IWMAddressAccess::GetAccessEntryCount, IWMAddressAccessGetAccessEntryCount, wmformat.iwmaddressaccess_getaccessentrycount, wmsdkidl/IWMAddressAccess::GetAccessEntryCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMAddressAccess.GetAccessEntryCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMAddressAccess::GetAccessEntryCount


## -description



The <b>GetAccessEntryCount</b> method retrieves the number of entries in the IP address access list.




## -parameters




### -param aeType [in]

A member of the <a href="https://msdn.microsoft.com/514e6745-c521-41bd-81c2-b6c24cfb0192">WM_AETYPE</a> enumeration specifying the type of entry (exclusion or inclusion).


### -param pcEntries [out]

Pointer to a variable that receives the number of entries of the type specified in <i>aeType</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7251c600-90a2-4903-b26a-643b4d10b0ce">IWMAddressAccess Interface</a>
 

 

