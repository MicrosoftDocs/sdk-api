---
UID: NF:wbemcli.IWbemServices.CreateClassEnumAsync
title: IWbemServices::CreateClassEnumAsync method
author: windows-driver-content
description: The IWbemServices::CreateClassEnumAsync method returns an enumeration of all classes that the class provider supports.
old-location: wmi\iwbemservices_createclassenumasync.htm
old-project: WmiSdk
ms.assetid: 02b81f48-c6a0-44db-86b9-936331b15cc4
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: CreateClassEnumAsync method [Windows Management Instrumentation], CreateClassEnumAsync method [Windows Management Instrumentation], IWbemServices interface, CreateClassEnumAsync,IWbemServices.CreateClassEnumAsync, IWbemServices, IWbemServices interface [Windows Management Instrumentation], CreateClassEnumAsync method, IWbemServices::CreateClassEnumAsync, WBEM_FLAG_BIDIRECTIONAL, WBEM_FLAG_DEEP, WBEM_FLAG_SEND_STATUS, WBEM_FLAG_SHALLOW, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_createclassenumasync, wbemcli/IWbemServices::CreateClassEnumAsync, wmi.iwbemservices_createclassenumasync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fastprox.dll
-	Esscli.dll
-	FrameDyn.dll
-	FrameDynOS.dll
-	Ntevt.dll
-	Stdprov.dll
-	Viewprov.dll
-	Wbemcomn.dll
-	Wbemcore.dll
-	Wbemess.dll
-	Wbemsvc.dll
-	Wmipicmp.dll
-	Wmidcprv.dll
-	Wmipjobj.dll
-	Wmiprvsd.dll
api_name:
-	IWbemServices.CreateClassEnumAsync
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemServices::CreateClassEnumAsync method


## -description


The 
<b>IWbemServices::CreateClassEnumAsync</b> method  returns an enumeration of all classes that the class provider supports. The class provider  creates each class definition from scratch and  only returns subclasses of the requested class. As an asynchronous method, 
<b>CreateClassEnumAsync</b> returns a status message immediately and then updates the sink passed through the <i>pResponseHandler</i> parameter—if necessary.

When a call succeeds, WMI calls <a href="_com_iunknown_addref">AddRef</a> on the pointer <i>pResponseHandler</i>, returns immediately, and  then asynchronously calls <i>pResponseHandler</i>– &gt;
<a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">Indicate</a> from another thread with class definitions until the query is satisfied.


## -parameters




### -param strSuperclass [in]

If not <b>NULL</b> or blank, this parameter specifies a parent class name. Only classes that are subclasses of this class are returned in the enumerator. If <b>NULL</b> or blank, and <i>lFlags</i> is <b>WBEM_FLAG_SHALLOW</b>, only top-level classes—those that have no parent class—are returned. If it is <b>NULL</b> or blank and <i>lFlags</i> is <b>WBEM_FLAG_DEEP</b>, all classes within the namespace are returned.


### -param lFlags [in]

One or more of the following values are valid.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, Windows Management Instrumentation (WMI) retrieves the amended qualifiers stored in the localized namespace of the current connection locale. If not set, only the qualifiers stored in the immediate namespace are retrieved.



#### WBEM_FLAG_BIDIRECTIONAL

This flag causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.



#### WBEM_FLAG_DEEP

This flag forces the enumeration to include this and all subclasses in the hierarchy.



#### WBEM_FLAG_SHALLOW

This flag forces the enumeration to include only pure instances of this class, excluding all instances of subclasses that supply properties not found in this class.



#### WBEM_FLAG_SEND_STATUS

This flag registers  a request in WMI to receive intermediate status reports through the client implementation of 
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">IWbemObjectSink::SetStatus</a>. Provider implementation must support intermediate status reporting for this flag to change behavior.

<div class="alert"><b>Note</b>  If <i>strSuperclass</i> is <b>NULL</b> or blank and <b>WBEM_FLAG_DEEP</b> is specified, all classes are returned.</div>
<div> </div>

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that can be used by the provider that returns the requested classes. The values in the context object must be specified in the documentation for the provider. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


### -param pResponseHandler [in]

Pointer to the caller implementation of 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>. This handler receives the objects as they become available by using the 
<a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">IWbemObjectSink::Indicate</a> method. When no  objects are available, the 
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">IWbemObjectSink::SetStatus</a> method is called by WMI. If any error code is returned, then the supplied 
<b>IWbemObjectSink</b> pointer is not used. If WBEM_S_NO_ERROR is returned, then the user 
<b>IWbemObjectSink</b> implementation is called to indicate the result of the operation. WMI only calls <b>AddRef</b> on the pointer when <b>WBEM_S_NO_ERROR</b> returns. When an error code returns, the reference count is the same as no entry. For a detailed explanation of this parameter, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. On failure, you can obtain available information from the COM function <a href=" http://go.microsoft.com/fwlink/p/?linkid=119575">GetErrorInfo</a>. COM-specific error codes  can be returned if network problems cause you to lose the remote connection to WMI. Note that if 
<b>CreateClassEnumAsync</b> returns WBEM_S_NO_ERROR, WMI waits for a result from the 
<b>SetStatus</b> method of the response handler. WMI waits indefinitely on a local connection or until a remote connection time-out occurs. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



Because the callback might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For more information about using methods semisynchronously, see <a href="https://msdn.microsoft.com/23122b38-5671-4454-be79-85c6bc34daa0">IWbemServices::CreateClassEnum</a> and <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### Examples

The following code example shows how to implement 
<b>CreateClassEnumAsync</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CStdProvider::CreateClassEnumAsync( 
            /* [in] */ BSTR strSuperclass,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler
            )
{
    IWbemClassObject *pClass = 0;

    // Assume there is an IWbemServices pointer available (m_pSvc).
    // Retrieve an 'empty' object that will be built up
    // into the class definition.
    
    HRESULT hRes = m_pSvc-&gt;GetObject(NULL, 0, NULL, &amp;pClass, 0);
    if (hRes)
    {
        return hRes;
    }

    // Prepare an empty object to receive the class definition.
        IWbemClassObject *pNextClass = 0;
        hRes = pClass-&gt;Clone(&amp;pNextClass);

    // Now loop through the private source of class definitions
    // and create each class.
    while(hRes)
    {
        // Create the class definition elsewhere.
        // For example, call a function that creates a definition:
        // FillClassDef(pNextClass);

        // Deliver the class to WMI.
        pResponseHandler-&gt;Indicate(1, &amp;pNextClass);
        pNextClass-&gt;Release( );

        // Prepare an empty object to receive the class definition.
        IWbemClassObject *pNextClass = 0;
        hRes = pClass-&gt;Clone(&amp;pNextClass);     
    }

    pClass-&gt;Release();

    // Send a finish message to WMI.

    pResponseHandler-&gt;SetStatus(0, hRes, 0, 0);

    return hRes;
}</pre>
</td>
</tr>
</table></span></div>
In the previous example, the class provider acquires a thread from WMI to perform the necessary operations. You may want to call the sink <a href="_com_iunknown_addref">AddRef</a> method and create another thread to deliver the objects in the result set. Creating another thread allows the current thread to return to WMI without depleting the thread pool. Whether the provider chooses the single thread design or the dual thread design depends on the amount of time the provider plans to use the WMI thread. There are no fixed rules. Experimentation can help you determine how your design affects WMI performance.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/23122b38-5671-4454-be79-85c6bc34daa0">IWbemServices::CreateClassEnum</a>



<a href="https://msdn.microsoft.com/f54b8e7c-c531-47d5-bab8-780652b94555">Retrieving an Error Code</a>
 

 

