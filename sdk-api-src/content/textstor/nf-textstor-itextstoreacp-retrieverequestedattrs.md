---
UID: NF:textstor.ITextStoreACP.RetrieveRequestedAttrs
title: ITextStoreACP::RetrieveRequestedAttrs
author: windows-driver-content
description: Gets the attributes returned by a call to an attribute request method.
old-location: tsf\itextstoreacp_retrieverequestedattrs.htm
old-project: TSF
ms.assetid: 6cd34ca5-6561-4161-beac-98248f0415f6
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],RetrieveRequestedAttrs method, ITextStoreACP.RetrieveRequestedAttrs, ITextStoreACP::RetrieveRequestedAttrs, RetrieveRequestedAttrs, RetrieveRequestedAttrs method [Text Services Framework], RetrieveRequestedAttrs method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_retrieverequestedattrs_ref, textstor/ITextStoreACP::RetrieveRequestedAttrs, tsf.itextstoreacp_retrieverequestedattrs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreACP.RetrieveRequestedAttrs
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP::RetrieveRequestedAttrs


## -description


Gets the attributes returned by a call to an attribute request method.


## -parameters




### -param ulCount [in]

Specifies the number of supported attributes to obtain.


### -param paAttrVals [out]

Pointer to the <a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL</a> structure that receives the supported attributes. The members of this structure depend upon the <i>dwFlags</i> parameter of the calling method.


### -param pcFetched [out]

Receives the number of supported attributes.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/39eb59cd-ec55-4057-8cf1-0203b6e6c82b">ITextStoreACP::RequestAttrsAtPosition
      </a>



<a href="https://msdn.microsoft.com/243cd002-c882-4ce9-b528-1a2229c46f4a">
        ITextStoreACP::RequestSupportedAttrs
      </a>



<a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">
        TS_ATTRVAL
      </a>



<a href="https://msdn.microsoft.com/ffd27e9b-3281-45a9-84f2-d09103689ced">
        TextStoreACP::RequestAttrsTransitioningAtPosition
      </a>
 

 

