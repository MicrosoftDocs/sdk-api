---
UID: NF:wmsdkidl.IWMLicenseRestore.CancelLicenseRestore
title: IWMLicenseRestore::CancelLicenseRestore method
author: windows-driver-content
description: The CancelLicenseRestore method cancels a current restore operation.
old-location: wmformat\iwmlicenserestore_cancellicenserestore.htm
old-project: wmformat
ms.assetid: b8a39804-5ee6-43ab-8e89-d1008217622d
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: CancelLicenseRestore method [windows Media Format], CancelLicenseRestore method [windows Media Format], IWMLicenseRestore interface, CancelLicenseRestore,IWMLicenseRestore.CancelLicenseRestore, IWMLicenseRestore, IWMLicenseRestore interface [windows Media Format], CancelLicenseRestore method, IWMLicenseRestore::CancelLicenseRestore, IWMLicenseRestoreCancelLicenseRestore, wmformat.iwmlicenserestore_cancellicenserestore, wmsdkidl/IWMLicenseRestore::CancelLicenseRestore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
-	IWMLicenseRestore.CancelLicenseRestore
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMLicenseRestore::CancelLicenseRestore method


## -description


<p class="CCE_Message">[<b>CancelLicenseRestore</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>CancelLicenseRestore</b> method cancels a current restore operation.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method operates asynchronously, and a call to this method cancels a restore operation that is in progress.




## -see-also




<a href="https://msdn.microsoft.com/29444445-7104-4900-a00d-dabd2766d1d7">IWMLicenseRestore Interface</a>
 

 

