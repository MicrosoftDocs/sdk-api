---
UID: NN:certenroll.IBinaryConverter
title: IBinaryConverter
author: windows-sdk-content
description: Contains general methods that enable you to create a Unicode-encoded string from a byte array, create a byte array from a Unicode-encoded string, and modify the type of Unicode encoding applied to a string.
old-location: security\ibinaryconverter.htm
tech.root: SecCertEnroll
ms.assetid: 495a321a-3005-4537-b082-5003e437d21f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBinaryConverter, IBinaryConverter interface [Security], IBinaryConverter interface [Security],described, certenroll/IBinaryConverter, security.ibinaryconverter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IBinaryConverter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBinaryConverter interface


## -description


The <b>IBinaryConverter</b> interface contains general methods that enable you to create a Unicode-encoded string from a byte array, create a byte array from a Unicode-encoded string, and modify the type of Unicode encoding applied to  a string. You can use this interface to represent a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate BLOB</a> as a printable string or to decode the string back into a certificate BLOB.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBinaryConverter</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IBinaryConverter</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IBinaryConverter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375201(v=VS.85).aspx">StringToString</a>
</td>
<td align="left" width="63%">
Modifies the type of Unicode encoding applied to a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375206(v=VS.85).aspx">StringToVariantByteArray</a>
</td>
<td align="left" width="63%">
Creates a byte array from a Unicode encoded string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375209(v=VS.85).aspx">VariantByteArrayToString</a>
</td>
<td align="left" width="63%">
Creates a Unicode encoded string from a byte array.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

