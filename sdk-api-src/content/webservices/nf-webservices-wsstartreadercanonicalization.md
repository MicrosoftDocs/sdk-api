---
UID: NF:webservices.WsStartReaderCanonicalization
title: WsStartReaderCanonicalization function
author: windows-sdk-content
description: This operation begins the process of putting the specified XML Reader in a standard or &#0034;canonized&#0034; form.
old-location: wsw\wsstartreadercanonicalization.htm
old-project: wsw
ms.assetid: 5dad9485-db3c-4ae0-b053-e1e4f32ad64d
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsStartReaderCanonicalization, WsStartReaderCanonicalization function [Web Services for Windows], webservices/WsStartReaderCanonicalization, wsw.wsstartreadercanonicalization
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsStartReaderCanonicalization
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsStartReaderCanonicalization function


## -description



        This operation begins the process  of putting the specified XML Reader in a standard or "canonized" form.
      


        The usage pattern for canonicalization is:

        <ul>
<li> Move the Reader to the element where canonicalization begins.
          </li>
<li> Call <b>WsStartReaderCanonicalization</b>.
          </li>
<li> Move the Reader forward to the end position.</li>
<li> Call <a href="https://msdn.microsoft.com/5cacad47-8581-4713-96cb-3b3a863e6327">WsEndReaderCanonicalization</a>.
        </li>
</ul>

        During this process the canonical bytes are written to the
        specified writeCallback.  <div class="alert"><b>Note</b>  Nodes advanced over
        are canonicalized including nodes of child elements skipped using <a href="https://msdn.microsoft.com/90eda6f1-dda2-4595-90f5-029768278f5b">WsSkipNode</a>. This is beneficial because it means that canonicalization and parsing can be done in one pass over
        the XML content regardless of what functions are used to read
        the data.
      </div>
<div> </div>



        In order to use the XML Reader solely
        for canonicalizing an XML element node the application can
        call <b>WsStartReaderCanonicalization</b>, <a href="https://msdn.microsoft.com/90eda6f1-dda2-4595-90f5-029768278f5b">WsSkipNode</a>
        and <a href="https://msdn.microsoft.com/5cacad47-8581-4713-96cb-3b3a863e6327">WsEndReaderCanonicalization</a> when the Reader is positioned
        on the element.
      <b>WsEndReaderCanonicalization</b> must be called in order to ensure that all
        canonicalized bytes are written to the specified callback.
      <div class="alert"><b>Note</b>  <code>WsEndReaderCanonicalization</code> must be called at the same depth at
        which <b>WsStartReaderCanonicalization</b>.  Other reader functions
        return an error if moved to a depth lower than where
        <b>WsStartReaderCanonicalization</b> was called.
      </div>
<div> </div>







        It is not valid to call <a href="https://msdn.microsoft.com/63d18407-f82b-4884-a162-2c8163e883e1">WsMoveReader</a> or <a href="https://msdn.microsoft.com/cc879cc0-c8ca-457e-9ff1-ae220e31cb04">WsSetReaderPosition</a> on a Reader between calls to <b>WsStartReaderCanonicalization</b> and <a href="https://msdn.microsoft.com/5cacad47-8581-4713-96cb-3b3a863e6327">WsEndReaderCanonicalization</a>.
      


## -parameters




### -param reader [in]

A pointer to the <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> object on which canonicalization is started.  The pointer must reference a valid <b>XML Reader</b> object.
                


### -param writeCallback [in]


          A  callback function invoked to write the canonical bytes as they are generated.
          <div class="alert"><b>Note</b>  This callback is invoked synchronously.</div>
<div> </div>



### -param writeCallbackState [in]

A pointer to a caller-defined state that is passed when invoking the <a href="https://msdn.microsoft.com/8d106ac2-226d-4e0c-8f14-8d3e17f15548">WS_WRITE_CALLBACK</a>.
        


### -param properties

An "array" reference of optional properties controlling how canonicalization is performed.  <div class="alert"><b>Note</b>  See <a href="https://msdn.microsoft.com/79f65ff2-4fa2-4808-b5cb-ad3aa6200260">WS_XML_CANONICALIZATION_PROPERTY</a> for details.</div>
<div> </div>



### -param propertyCount [in]

The number of properties.


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">

The operation is not allowed due to the current state of the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">

The input data was not in the expected format or did not have the expected value.

</td>
</tr>
</table>
 




## -remarks




        Calls to this function cannot be nested.  Consequently a call to <b>WsStartReaderCanonicalization</b> must be followed by a call to <a href="https://msdn.microsoft.com/5cacad47-8581-4713-96cb-3b3a863e6327">WsEndReaderCanonicalization</a> before the next <b>WsStartReaderCanonicalization</b> call can be made.
      


        If a <a href="https://msdn.microsoft.com/230e4b9d-f6ce-45a8-9efd-2a6949d3e6f4">WS_XML_CANONICALIZATION_ALGORITHM</a> is not specified <b>WS_EXCLUSIVE_XML_CANONICALIZATION_ALGORITHM</b> is used.
      


        The <b>WS_INCLUSIVE_XML_CANONICALIZATION_ALGORITHM</b> and 
        <b>WS_INCLUSIVE_WITH_COMMENTS_XML_CANONICALIZATION_ALGORITHM</b> algorithms can only be used with
        entire XML documents.  The Reader must be positioned at <b>WS_XML_NODE_TYPE_BOF</b> when
        <b>WsStartReaderCanonicalization</b> is called with these algorithms.
      



