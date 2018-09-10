---
UID: NF:oleauto.CreateDispTypeInfo
title: CreateDispTypeInfo function
author: windows-sdk-content
description: Creates simplified type information for use in an implementation of IDispatch.
old-location: automat\createdisptypeinfo.htm
tech.root: automat
ms.assetid: 603e00e8-0370-4ebf-b9d2-85e6e58c2b3a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateDispTypeInfo, CreateDispTypeInfo function [Automation], _oa96_CreateDispTypeInfo, automat.createdisptypeinfo, oleauto/CreateDispTypeInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - CreateDispTypeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateDispTypeInfo function


## -description


Creates simplified type information for use in an implementation of <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>.


## -parameters




### -param pidata

The interface description that this type information describes.




### -param lcid

The locale identifier for the names used in the type information.




### -param pptinfo

On return, pointer to a type information implementation for use in <a href="https://msdn.microsoft.com/720a0237-9c68-4252-9f66-43610d4be106">DispGetIDsOfNames</a> and <a href="https://msdn.microsoft.com/69b89e5c-2a04-4a6a-beb0-18e68f8866ac">DispInvoke</a>.


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
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
The interface is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
Either the interface description or the LCID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



You can construct type information at run time by using <b>CreateDispTypeInfo</b> and an INTERFACEDATA structure that describes the object being exposed.

The type information returned by this function is primarily designed to automate the implementation of <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>. <b>CreateDispTypeInfo</b> does not return all of the type information described in <a href="https://msdn.microsoft.com/ab44422c-97d6-4a63-ade1-db919d53aae7">Type Description Interfaces</a>. The argument <i>pidata</i> is not a complete description of an interface. It does not include Help information, comments, optional parameters, and other type information that is useful in different contexts.

Accordingly, the recommended method for providing type information about an object is to describe the object using the Object Description Language (ODL), and to compile the object description into a type library using the Microsoft Interface Definition Language (MIDL) compiler.

To use type information from a type library, use the <a href="https://msdn.microsoft.com/155b48e5-5438-409e-9342-630a6a500f60">LoadTypeLib</a> and <a href="https://msdn.microsoft.com/58f96322-f1cd-448c-906d-b7faa65ab9a0">GetTypeInfoOfGuid</a> functions instead of <b>CreateDispTypeInfo</b>. For more information <a href="https://msdn.microsoft.com/ab44422c-97d6-4a63-ade1-db919d53aae7">Type Description Interfaces</a>. 


#### Examples

The code that follows creates type information from INTERFACEDATA to expose the CCalc object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>static METHODDATA NEARDATA rgmdataCCalc[] =
{
      PROPERTY(VALUE,  IMETH_ACCUM,    IDMEMBER_ACCUM,    VT_I4),
      PROPERTY(ACCUM,  IMETH_ACCUM,    IDMEMBER_ACCUM,    VT_I4),
      PROPERTY(OPND,   IMETH_OPERAND,  IDMEMBER_OPERAND,  VT_I4),
      PROPERTY(OP,     IMETH_OPERATOR, IDMEMBER_OPERATOR, VT_I2),
      METHOD0(EVAL,    IMETH_EVAL,     IDMEMBER_EVAL,     VT_BOOL),
      METHOD0(CLEAR,   IMETH_CLEAR,    IDMEMBER_CLEAR,    VT_EMPTY),
      METHOD0(DISPLAY, IMETH_DISPLAY,  IDMEMBER_DISPLAY,  VT_EMPTY),
      METHOD0(QUIT,    IMETH_QUIT,     IDMEMBER_QUIT,     VT_EMPTY),
      METHOD1(BUTTON,  IMETH_BUTTON,   IDMEMBER_BUTTON,   VT_BOOL),
};

INTERFACEDATA NEARDATA g_idataCCalc =
{
   rgmdataCCalc, DIM(rgmdataCCalc)
};

// Use Dispatch interface API functions to implement IDispatch.
CCalc *
CCalc::Create()
{
   HRESULT hresult;
   CCalc * pcalc;
   CArith * parith;
   ITypeInfo * ptinfo;
   IUnknown * punkStdDisp;
   extern INTERFACEDATA NEARDATA g_idataCCalc;

   if((pcalc = new CCalc()) == NULL)
      return NULL;
   pcalc-&gt;AddRef();

   parith = &amp;(pcalc-&gt;m_arith);

   // Build type information for the functionality on this object that
   // is being exposed for external programmability.
   hresult = CreateDispTypeInfo(
      &amp;g_idataCCalc, LOCALE_SYSTEM_DEFAULT, &amp;ptinfo);
   if(hresult != NOERROR)
      goto LError0;

   // Create an aggregate with an instance of the default
   // implementation of IDispatch that is initialized with 
   // type information.
   hresult = CreateStdDispatch(
      pcalc,            // Controlling unknown.
      parith,            // Instance to dispatch on.
      ptinfo,            // Type information describing the instance.
      &amp;punkStdDisp);

   ptinfo-&gt;Release();

   if(hresult != NOERROR)
      goto LError0;

   pcalc-&gt;m_punkStdDisp = punkStdDisp;

   return pcalc;

LError0:;
   pcalc-&gt;Release();
   return NULL;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2c66b04e-9d96-45e9-8105-82d58a5a4085">Creation of Dispatch API Functions</a>



<a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

