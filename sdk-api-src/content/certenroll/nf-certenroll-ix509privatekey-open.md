---
UID: NF:certenroll.IX509PrivateKey.Open
title: IX509PrivateKey::Open
author: windows-sdk-content
description: Opens an existing private key.
old-location: security\ix509privatekey_open_method.htm
tech.root: SecCertEnroll
ms.assetid: 965e3bf8-22b9-4015-8fb2-102c5f7b1cb5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509PrivateKey interface [Security],Open method, IX509PrivateKey.Open, IX509PrivateKey::Open, Open, Open method [Security], Open method [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::Open, security.ix509privatekey_open_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IX509PrivateKey.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PrivateKey::Open


## -description


The <b>Open</b> method opens an existing <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a>.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



If successful, this method sets the <a href="https://msdn.microsoft.com/en-us/library/Aa379026(v=VS.85).aspx">Opened</a> property. You must call either the <b>Open</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa378957(v=VS.85).aspx">Create</a> methods before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa379006(v=VS.85).aspx">Export</a> method or <a href="https://msdn.microsoft.com/en-us/library/Aa379003(v=VS.85).aspx">ExportPublicKey</a> method.

You cannot set the following properties after calling the <b>Open</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa378957(v=VS.85).aspx">Create</a> methods. If you wish to specify them, you must do so before calling either of these methods.<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378926(v=VS.85).aspx">Algorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378953(v=VS.85).aspx">ContainerName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378946(v=VS.85).aspx">ContainerNamePrefix</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378966(v=VS.85).aspx">CspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378972(v=VS.85).aspx">CspStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa965843(v=VS.85).aspx">Description</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378993(v=VS.85).aspx">Existing</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379002(v=VS.85).aspx">ExportPolicy</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa965844(v=VS.85).aspx">FriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379019(v=VS.85).aspx">KeyProtection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379021(v=VS.85).aspx">KeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379022(v=VS.85).aspx">LegacyCsp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379023(v=VS.85).aspx">Length</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379024(v=VS.85).aspx">MachineContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379031(v=VS.85).aspx">ProviderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379032(v=VS.85).aspx">ProviderType</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379029(v=VS.85).aspx">Pin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379033(v=VS.85).aspx">ReaderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379035(v=VS.85).aspx">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379036(v=VS.85).aspx">UIContextMessage</a>
</li>
</ul>


The following properties can be set regardless of whether the key is open:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378928(v=VS.85).aspx">Certificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379028(v=VS.85).aspx">ParentWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379034(v=VS.85).aspx">SecurityDescriptor</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 

